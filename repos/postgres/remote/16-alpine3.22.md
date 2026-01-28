## `postgres:16-alpine3.22`

```console
$ docker pull postgres@sha256:b9264fe004923f2096e6a2dab20fa0305f6302fd1456a773a0c0bc93174bc61b
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

### `postgres:16-alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:ef1306c4c60c19ffe3d88e42028665c72dcc87cf7af068a93f01ca0d995c1d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109492769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61e956c480fe7b58e98033a69bc11576b8b67850f956404fda2bff72b1b1dc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:30:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:30:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:30:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:30:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:30:47 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:30:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:30:47 GMT
ENV PG_MAJOR=16
# Wed, 28 Jan 2026 02:30:47 GMT
ENV PG_VERSION=16.11
# Wed, 28 Jan 2026 02:30:47 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Wed, 28 Jan 2026 02:30:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:33:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:33:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:33:15 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:33:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:33:15 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:33:15 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:33:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:33:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:33:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:33:15 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:33:15 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:33:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd86c0dc10268cc02c9c5461e132a8f5e09da83375a21b462948bb50408f2bd0`  
		Last Modified: Wed, 28 Jan 2026 02:33:31 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf559938013dc69be371c3cfdafd1afe71bdb1783ab4081a94fcf4d3213305f`  
		Last Modified: Wed, 28 Jan 2026 02:33:32 GMT  
		Size: 918.3 KB (918291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e007e612c5da65b3b3dc851ab8a29768ba4f8182f79d418a9f22d8ba6bbdcdaa`  
		Last Modified: Wed, 28 Jan 2026 02:33:31 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d4f01f176f54b2cd2c67c7f8ad4189f3ef5f83744c1029602c2001bf67f9c0`  
		Last Modified: Wed, 28 Jan 2026 02:33:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7677dddaf293ee4087b186f95aa7bd755ff885f7aeb89008d3c2e5fa24da2d66`  
		Last Modified: Wed, 28 Jan 2026 02:33:36 GMT  
		Size: 104.8 MB (104752464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3ff2f980f17e8a8a0925d177fb646af1f19341cac79a15703cd07d55603af9`  
		Last Modified: Wed, 28 Jan 2026 02:33:33 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c47c6d875410af71ef9199bd26531d49c2009962aa2dd6f0563636e17e09f11`  
		Last Modified: Wed, 28 Jan 2026 02:33:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940d6769493f3a7f3a8d840a5f958892d21dc6e651ba7c3f4294fd9a7f75b898`  
		Last Modified: Wed, 28 Jan 2026 02:33:33 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f412b7f8d4597f964bdc02f7d67e6f3d1004333ef0e9a812669838a1960e6cc8`  
		Last Modified: Wed, 28 Jan 2026 02:33:34 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4832f99c5f6f3d07a552cce49ab37568f996c005f343bb1553ee99eb01fb31f`  
		Last Modified: Wed, 28 Jan 2026 02:33:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:b9a6519e37ca56e2500b96e228d358efc7c067a5294a2eb5375e5cbe61a84bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (639999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f8a4df6c4f7adeef11a3776a6c5c57b1fe41bcb7372496fd1fa3cb33e280ab`

```dockerfile
```

-	Layers:
	-	`sha256:9413888a4989d6f261f8cc147ab1f42268704c247fb69d2fe184615858319b39`  
		Last Modified: Wed, 28 Jan 2026 02:33:31 GMT  
		Size: 596.3 KB (596315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26142e6504c1c2d388e15f6cccf9a45c07ef6c9bbbea9099fc0a14cd875d1652`  
		Last Modified: Wed, 28 Jan 2026 02:33:31 GMT  
		Size: 43.7 KB (43684 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:d86640e0f7fcb80762d8218be133d717972796240bcd41f36d5a99876d31e111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (89034841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef153546179e7472b5de968568ce61c14669ebe394a683da6fa4f5779c6e9f29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 19:40:22 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:40:25 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:40:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:40:26 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 19:40:26 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:40:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:40:26 GMT
ENV PG_MAJOR=16
# Fri, 14 Nov 2025 19:40:26 GMT
ENV PG_VERSION=16.11
# Fri, 14 Nov 2025 19:40:26 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Fri, 14 Nov 2025 19:40:26 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 19:43:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:43:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:43:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:43:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:43:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:43:14 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:43:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:43:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:43:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:43:14 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:43:14 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:43:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:10 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5037c0bbdbcc5878d7c934a45a9f46b8a1032f69c780f63f26e8ff56ec8103b`  
		Last Modified: Fri, 14 Nov 2025 19:43:25 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25758288a4ae90ea567c95e85347e0ad89dfdf3f9ad80122f804847c6655ea3a`  
		Last Modified: Fri, 14 Nov 2025 19:43:25 GMT  
		Size: 886.1 KB (886134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002a0b60e045fc45ff75aeb01c83aa106515a54907bd0be97895f952bd43ea91`  
		Last Modified: Fri, 14 Nov 2025 19:43:25 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92b21faf2ce157c5b455aaf148add1c37dbadb05fab9dda73a50097143edb4b`  
		Last Modified: Fri, 14 Nov 2025 19:43:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67beca2d05f8894136b9da1c27d7d1e3e1b41fc3fa1633006cdb6cf75a032e99`  
		Last Modified: Fri, 14 Nov 2025 19:43:28 GMT  
		Size: 84.6 MB (84627481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22594a682984617bb166a0115ec4917f1edc3ffd3c72a1ec26ab936f769a7965`  
		Last Modified: Fri, 14 Nov 2025 19:43:26 GMT  
		Size: 9.6 KB (9562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8985b4220db637ffd148d3d0d83784c41e2f4a9939f7b5bef5bad1fcf98545f1`  
		Last Modified: Fri, 14 Nov 2025 19:43:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97f984f4ede5076a864abcf21ba5bb4e2da43c908392f3b1ce1f7aae269e4c0`  
		Last Modified: Fri, 14 Nov 2025 19:43:26 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad596fab345e37634df46db9c953d83e36beae9ae588ffbdb46228220e8cc56`  
		Last Modified: Fri, 14 Nov 2025 19:43:27 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3429b7f21f4841c8b9dd68bc17299c780697f1b445739cc73abbb0c4acbf31`  
		Last Modified: Fri, 14 Nov 2025 19:43:27 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:384c876cb073f0ec55bedb089868f335f8d9b7fe80ca2422503aabbdce2961b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 KB (44269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86de7fc3ff67594479a172b5ef5c18bcde851cabb1287ac6b1be9d9d5dea90fd`

```dockerfile
```

-	Layers:
	-	`sha256:87899cbec216a6c3cf1168c6611e0851196690832a20782dad06d9d227f85d1f`  
		Last Modified: Fri, 14 Nov 2025 19:43:25 GMT  
		Size: 44.3 KB (44269 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:74211d48e0e80c62636c77de7d8dc206b12ecc0dbbec3afbebbb609e05b17c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84307519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16751ec60c9c9930c99c233a737f130d849570dcd56e9618fd2c1defc8edb08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:47:34 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:47:37 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:47:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:47:37 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:47:37 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:47:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:47:37 GMT
ENV PG_MAJOR=16
# Wed, 28 Jan 2026 02:47:37 GMT
ENV PG_VERSION=16.11
# Wed, 28 Jan 2026 02:47:37 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Wed, 28 Jan 2026 02:47:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:50:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:50:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:50:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:50:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:50:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:50:25 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:50:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:50:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:50:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:50:25 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:50:25 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:50:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d11c7d54593fec235a1bdb568a564023789fd0bb94a1dc26539e45e786374a8`  
		Last Modified: Wed, 28 Jan 2026 02:50:37 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d50a83407a48f53d23b76bd31aaa272be51d2bdd39d9199203290e160f66a35`  
		Last Modified: Wed, 28 Jan 2026 02:50:37 GMT  
		Size: 886.1 KB (886132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1763bee7cdab6709c2736ab9d3d7ca6c07497e5b03e70c26fc6fd772e9d747`  
		Last Modified: Wed, 28 Jan 2026 02:50:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce26d66ba2add6a0d83394af5be551f51cd953636ca3db1fb7692cd69145cfa`  
		Last Modified: Wed, 28 Jan 2026 02:50:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f587f0ebf51310f0899749a091e355d1ed53dc1ec36b78f0f8ff7698a32f457e`  
		Last Modified: Wed, 28 Jan 2026 02:50:40 GMT  
		Size: 80.2 MB (80180619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9bf5005929576b846948263db58f7d4f661f638032b0e2d592b51ab25e76ca`  
		Last Modified: Wed, 28 Jan 2026 02:50:38 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8dacd1e6ff7e008330bfb844ab331377fa9e998ed0187ba22998c2d32b6feb`  
		Last Modified: Wed, 28 Jan 2026 02:50:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60af2be8ccdf25736b06ce74ac2a0bce294b0c99e30ad138b3c8526c459f3311`  
		Last Modified: Wed, 28 Jan 2026 02:50:38 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587442808d0ecc3e06dd2f3a73a3b2566b0077665d55b5c1ba184a3ef4bfdace`  
		Last Modified: Wed, 28 Jan 2026 02:50:39 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd83cfafc7e1a5771722bfebc27a32b7e72c00feab55a66312b68384013da3d7`  
		Last Modified: Wed, 28 Jan 2026 02:50:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:794d01dc8b80ce375375bfd0f27151cd13dd65a6d784dac50717257acf3f1cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f168ac4f7b209afd24af78bf3c9d653a88ee87d701900434c14de606c572139`

```dockerfile
```

-	Layers:
	-	`sha256:a83b3bb7317306d5fadbed15efa5260451e9908696c1d0d8535f4820fc90c285`  
		Last Modified: Wed, 28 Jan 2026 02:50:37 GMT  
		Size: 596.3 KB (596335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59cd6cd845cc4af8a46fccbcad65533714621d69bbd71e376e22308f8f7c16e7`  
		Last Modified: Wed, 28 Jan 2026 02:50:37 GMT  
		Size: 43.8 KB (43846 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:9140cc382901a554fea7ef1b263df355035dde3ec49fe64583271478a01a1c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105451880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0672e71f4963ea9d62bfc50da67939482664393cf14463d47e3ef367abfbeb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:32:29 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:32:32 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:32:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:32:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:32:32 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:32:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:32:32 GMT
ENV PG_MAJOR=16
# Wed, 28 Jan 2026 02:32:32 GMT
ENV PG_VERSION=16.11
# Wed, 28 Jan 2026 02:32:32 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Wed, 28 Jan 2026 02:32:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:35:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:35:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:35:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:35:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:35:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:35:18 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:35:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:35:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:35:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:35:18 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:35:18 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:35:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0ef7cc186b508aad0da7dc4540d4dc87e7d4f68f404c80c8548a4db224a32e`  
		Last Modified: Wed, 28 Jan 2026 02:35:32 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb77fe54524d1887b9c828d7532c44f4e642afc7fa83da87c3fc36b4ba2dd46`  
		Last Modified: Wed, 28 Jan 2026 02:35:32 GMT  
		Size: 873.5 KB (873487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabd5adff40d5a076ce54254324ae842578b46762eb87e2229f204216e0f0030`  
		Last Modified: Wed, 28 Jan 2026 02:35:32 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c289b1a5684d7419037c1f2316cdada64f39f36e5abe0f307950cb1fe873cbf`  
		Last Modified: Wed, 28 Jan 2026 02:35:05 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d7303476c3d6aa974769d268fed105c4d7973b33d2cad9033a5845e5c4e0d9`  
		Last Modified: Wed, 28 Jan 2026 02:35:36 GMT  
		Size: 100.4 MB (100421738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ec7697d5175fb8e06f39e2f2d0e573ad4b5b60c8ff4c13d5afacbe2f6872d4`  
		Last Modified: Wed, 28 Jan 2026 02:35:33 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1154988e2077fc8c8afe621aeb09ad7f9c2917eb996535faf407ac961ac72b81`  
		Last Modified: Wed, 28 Jan 2026 02:35:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b46c405cd2df54f53267f642e4c32d0ed7d78bbbc6353944810634726544fb`  
		Last Modified: Wed, 28 Jan 2026 02:35:34 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49acd221538c8a2d0f18870e42f7c198cb8c655fbcf1d5ae12490a5281ec825`  
		Last Modified: Wed, 28 Jan 2026 02:35:34 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f23b7d66f67904d216ecae7feb8219494c404aa96c59f30c888793c85fd2376`  
		Last Modified: Wed, 28 Jan 2026 02:35:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:5eb7567945572691ec4d2f10f5ac0a73e017ba26599b1dfe9a1e0d3e00718a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6085dd50a8062ce19908b2a4b4372c9dbd14682f77c48188bacf50bb8ed3c2ec`

```dockerfile
```

-	Layers:
	-	`sha256:d6a5431fe29e36d9e8b0ff66b4eb2d09d659585e97b29210a98bc138ed9bce28`  
		Last Modified: Wed, 28 Jan 2026 02:35:32 GMT  
		Size: 596.3 KB (596347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:372b9886b8972e58b54652bab95fed6300f882b06332abc6c32b69b2b0710beb`  
		Last Modified: Wed, 28 Jan 2026 02:35:32 GMT  
		Size: 43.9 KB (43882 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:a3d5e3856de372648b7c46384460103bf178a30ce0d1b5c60052a6ad6b9fb987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115728010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77c05b9cea89d2d9a18b984aaa6b63d541edeb2cffc1fd4cffea4634cc9d182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:27:54 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:27:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:27:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:27:57 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 02:27:57 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:27:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:27:57 GMT
ENV PG_MAJOR=16
# Wed, 28 Jan 2026 02:27:57 GMT
ENV PG_VERSION=16.11
# Wed, 28 Jan 2026 02:27:57 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Wed, 28 Jan 2026 02:27:57 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:30:35 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:30:35 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:30:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:30:35 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:30:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:30:35 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:30:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:30:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:30:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:30:35 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:30:35 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:30:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277c009459198dbdb5ab2cdb4a943df6164d9eadfc1bc24f0d825eac8b6868ae`  
		Last Modified: Wed, 28 Jan 2026 02:30:18 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e2147a93acfdc3c66e254188497c336a88f57acffef3258b0bbad1889cf6d5`  
		Last Modified: Wed, 28 Jan 2026 02:30:52 GMT  
		Size: 890.6 KB (890626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5baa5f3f88ef4ee60f5735fea66e46e88d8f25a20d6b7eed61641756b332a3d`  
		Last Modified: Wed, 28 Jan 2026 02:30:52 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58de2ded5529ce062b3a0f29b6c058600b95c80629a35dc4d4b0f0e1a9b0e2b`  
		Last Modified: Wed, 28 Jan 2026 02:30:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13dc22f005a7f1c16a3c612a9d3eba3a6717083b9b653d1b62206b605098facc`  
		Last Modified: Wed, 28 Jan 2026 02:30:54 GMT  
		Size: 111.2 MB (111199511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983c5cab2873e8895d967dfe51706a05049c3ee585cef93ef98a8a1f4a2f6c7a`  
		Last Modified: Wed, 28 Jan 2026 02:30:52 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9630afbae46b85dc8ea95e3f0ff280d1b843ce8f1b697caf4a8f80e417f3fd14`  
		Last Modified: Wed, 28 Jan 2026 02:30:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6537c02a921e046098d8069618d0965fefeffc601ab71b74c50b92100906ff`  
		Last Modified: Wed, 28 Jan 2026 02:30:53 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0276bddb43feab3282a3faf53bcd08beb10903a024dc99d2788ae2e6abd20469`  
		Last Modified: Wed, 28 Jan 2026 02:30:53 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035e0c642e5dcd2ef6cd9f99249799223deda7f2ab715921fab653139d046ac3`  
		Last Modified: Wed, 28 Jan 2026 02:30:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:5be1e86320796651063bd3e292489f81678b5f4aaa588d7f4a12b2389e79b681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.9 KB (639944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbf191563badd99ae23e0b1e6489cd0696f7786b9cfbc28cea7e4a662b27f96`

```dockerfile
```

-	Layers:
	-	`sha256:3321c91cedd3704871fc2b2ef92522c1b4f2798335c0d2887172d7b38b9aae25`  
		Last Modified: Wed, 28 Jan 2026 02:30:52 GMT  
		Size: 596.3 KB (596300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb0745544ab09b9d7d14f952b96809022af79cdc4a58eda28565cd6c9fe79115`  
		Last Modified: Wed, 28 Jan 2026 02:30:52 GMT  
		Size: 43.6 KB (43644 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:959dd1dd8580624feac63895629461a5ad1818dbbdbb76382a33fb997a79c026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93259245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d653873478daf1c437f31929d4ade9d6aec0c9f34600ecaede26e210f9878e9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:33:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 03:33:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 03:33:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 03:41:23 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 28 Jan 2026 03:41:23 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 03:41:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 03:41:23 GMT
ENV PG_MAJOR=16
# Wed, 28 Jan 2026 03:41:23 GMT
ENV PG_VERSION=16.11
# Wed, 28 Jan 2026 03:41:23 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Wed, 28 Jan 2026 03:41:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 03:44:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 03:44:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 03:44:15 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 03:44:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 03:44:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 03:44:16 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 03:44:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:44:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 03:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:44:17 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 03:44:17 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 03:44:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cf718fa459d8840034db063bb9424e81c3d9174a32a4c9dfc267b33036ad07`  
		Last Modified: Wed, 28 Jan 2026 03:36:40 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9227b35430cc92748ff2ebf224e67d8d43cd96411ecdffb11f93f8780a00bd1e`  
		Last Modified: Wed, 28 Jan 2026 03:36:40 GMT  
		Size: 879.0 KB (879034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb8caad2d394d40c900318205bb2a4fab84cb8a4174174889d0d3ba8cd34ec9`  
		Last Modified: Wed, 28 Jan 2026 03:44:43 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea567f655947b15a81f4906d157299d55233dbc5ed74ff062f795cda2c2b610c`  
		Last Modified: Wed, 28 Jan 2026 03:44:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65653971b70e622072f00642664cb9437ea26adecd7260c878b420043ea927d`  
		Last Modified: Wed, 28 Jan 2026 03:44:46 GMT  
		Size: 88.6 MB (88628764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e35faf0bcd4565a916a3a78a144f310a725dbc31ae07256abd4055bbec87080`  
		Last Modified: Wed, 28 Jan 2026 03:44:43 GMT  
		Size: 9.6 KB (9565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e76f474e9270bc7bfe419113a9a90011e790a41fdea6b46d69b17583bc39bfb`  
		Last Modified: Wed, 28 Jan 2026 03:44:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfa68d75d93204c39e1df54903ac9154724f11183adcb1a6813ecea0f803f89`  
		Last Modified: Wed, 28 Jan 2026 03:44:45 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ceae4110e20dd3f94afe1c778f691fd120a5e66f3ad78fc2eeb11991e71cbb9`  
		Last Modified: Wed, 28 Jan 2026 03:44:45 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2961c7cf41b2b808e56ae6115039894d8f2efae6111d83cceb96ac577feb29e`  
		Last Modified: Wed, 28 Jan 2026 03:44:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:27813fa62c561ed6d8e4f6848188a7cadaa6e8d184fe8163e986f85f642e1f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.5 KB (636450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06fb2ad84d8d4e5e9ce2805d6f2cb3b6fedacaedad271bf444168b0e57b0fee`

```dockerfile
```

-	Layers:
	-	`sha256:6b4a386cf76b15c5a56f195428e23909de67876ee9476e59d96d1a776bd114f2`  
		Last Modified: Wed, 28 Jan 2026 03:44:43 GMT  
		Size: 592.7 KB (592724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:433ca1d3be63c17a353b4705a80963f8a4b2ccb8db288d3891739c42251ce844`  
		Last Modified: Wed, 28 Jan 2026 03:44:43 GMT  
		Size: 43.7 KB (43726 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:0cedfbc501d38828a3ac8f9a05b7281f5b35f3d573cc8f8688bb6467cb6edc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109495085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51cfb9f11d93a75d0f8bf7ca25489c60c0b5760ab8fc04f00ed72df239a76496`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 00:10:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 00:10:13 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 00:10:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 07:42:02 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 07:42:02 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 07:42:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 07:42:02 GMT
ENV PG_MAJOR=16
# Fri, 14 Nov 2025 07:42:02 GMT
ENV PG_VERSION=16.11
# Fri, 14 Nov 2025 07:42:02 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Fri, 14 Nov 2025 07:42:02 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 08:31:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 08:31:29 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 08:31:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 08:31:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 08:31:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 08:31:30 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 15 Nov 2025 07:42:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 15 Nov 2025 07:42:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 15 Nov 2025 07:42:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 15 Nov 2025 07:42:38 GMT
STOPSIGNAL SIGINT
# Sat, 15 Nov 2025 07:42:38 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 15 Nov 2025 07:42:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:17:39 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d16d13f9766542076f489b4bde8f2b9299f759730ca1132f12a478b4ab5317`  
		Last Modified: Fri, 14 Nov 2025 01:02:08 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f681bb079be6f40bd7adede139f20494c17a8116703e2d4d80cdafbeac44ec0f`  
		Last Modified: Fri, 14 Nov 2025 01:02:09 GMT  
		Size: 866.6 KB (866631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61568bffe09594f38a4358fa0027d359c02c9e9664c5e3da06f4814c0e9823a`  
		Last Modified: Fri, 14 Nov 2025 08:34:15 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f405327ef14efadeef909f0df17348553c8e2b5d4662f91456b23d19d7fe6218`  
		Last Modified: Fri, 14 Nov 2025 08:34:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc32372c630598e9c32e0489613a2ccab3abb48679f36a463a8c2a392e4d6dca`  
		Last Modified: Fri, 14 Nov 2025 08:34:31 GMT  
		Size: 105.1 MB (105096049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a4dba820ccef32b476f89043cbc0d795b96f8d6be79713de715738c19f746d`  
		Last Modified: Fri, 14 Nov 2025 08:34:15 GMT  
		Size: 9.6 KB (9567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1878f9b5ab09ee7d689bb2c7f89959074e3bfc5d26bbd3e53ec7e3e5a49614b4`  
		Last Modified: Fri, 14 Nov 2025 08:34:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fb5ee143a12e841a8b10476fb1bddc316d1b212b4d2e793428becc35bfc34c`  
		Last Modified: Fri, 14 Nov 2025 08:34:16 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f962459f3c54d9fad80b2fd4685fb8381b178db08b221138560c9c1a3fdc8f`  
		Last Modified: Sat, 15 Nov 2025 07:43:54 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d88fb469e6d5ef194abb7c581fc9a7ea64ff792ba35694d9080678d5329af83`  
		Last Modified: Sat, 15 Nov 2025 07:43:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:4779282dae47e559f8c87b512388ce251d14dfedfdbbf90a3488d80d189582f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.4 KB (639382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e24fa4da9afbd3d59f05004f24764cd2a979e290fc0c0965cc03e475b94644`

```dockerfile
```

-	Layers:
	-	`sha256:5d6f9e3d9424f932344adc5dfd66b129037b49d573f18451b56d79ed7943255a`  
		Last Modified: Sat, 15 Nov 2025 07:43:54 GMT  
		Size: 595.0 KB (595016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a20efac8e9b6c4dbab617861c8018dbe7ec405292835b52af92e2377a0493b0`  
		Last Modified: Sat, 15 Nov 2025 07:43:53 GMT  
		Size: 44.4 KB (44366 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:f8335d4599dbb92ce14777179b57e05a7ec9b20d626bef6a4ebe604fa149fa24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118182642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec5fd92433549f1041d894a195ab99b165fbc1e4ac80df63f1f281fc58e387f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 01:24:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 01:24:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 01:24:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 01:24:12 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 14 Nov 2025 01:24:12 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 01:24:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 01:24:12 GMT
ENV PG_MAJOR=16
# Fri, 14 Nov 2025 01:24:12 GMT
ENV PG_VERSION=16.11
# Fri, 14 Nov 2025 01:24:12 GMT
ENV PG_SHA256=6deb08c23d03d77d8f8bd1c14049eeef64aef8968fd8891df2dfc0b42f178eac
# Fri, 14 Nov 2025 01:24:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 01:27:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 01:27:03 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 01:27:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 01:27:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 01:27:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 01:27:03 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:34:45 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:34:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:34:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:34:45 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:34:45 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:34:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:18 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d27f93166421531fe4a5435a9bca3ea4e7a361893fc542ed1fd5124e07175f`  
		Last Modified: Fri, 14 Nov 2025 01:27:26 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5428b16fd632d91d3982d2d488bfbd69daf3b4db82a5d75683ec8a2731260b2b`  
		Last Modified: Fri, 14 Nov 2025 01:27:26 GMT  
		Size: 894.4 KB (894417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d26e50aab688246007d981ec03ed0f2ba085e93831f3c2b4a5c41cedb4f6ab4`  
		Last Modified: Fri, 14 Nov 2025 01:27:26 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d3fda138bdb19608f3408a47a5ceb1f1e5a70ee029d664c864ace4ba7e8e7d`  
		Last Modified: Fri, 14 Nov 2025 01:27:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79779a960d52b35c2f91a115ab8fe036b19a4a7e4b508b7441700e92ad62a87a`  
		Last Modified: Fri, 14 Nov 2025 01:27:29 GMT  
		Size: 113.6 MB (113621832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff89726acd5d172f80f564aafa849445c779716f5e7a5ba43bad42ee611a3f99`  
		Last Modified: Fri, 14 Nov 2025 01:27:27 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94f9a9f0b8e91e38655eb80d2cb19ad6a68edea804e7bdeb638dce8e3fae7fd`  
		Last Modified: Fri, 14 Nov 2025 01:27:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd213bb65324f3224ed18db3ff9adf080dc14ec4c06e0ea97ef0210eb4c1c9f9`  
		Last Modified: Fri, 14 Nov 2025 01:27:28 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e761d1e0f28417e8426745276702840f5955d0dbe5190ec8821bfa637d57b77`  
		Last Modified: Fri, 14 Nov 2025 19:34:57 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bf0fafd2a2b7997999676bec76d3e345628876ddbd919365f43a589177b563`  
		Last Modified: Fri, 14 Nov 2025 19:34:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:113760a14075e61c4e0b097030ad5a7c904be573062dae9a02e4bc2123bdb34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.3 KB (639292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42a746e46cc775a85000c4db755da80247989263814899c4d33b1f39509e197`

```dockerfile
```

-	Layers:
	-	`sha256:bb1fee8596dafb1318fe41be8d30677271c69d61f93ee8b5a2127ad3be3c47a2`  
		Last Modified: Fri, 14 Nov 2025 19:34:57 GMT  
		Size: 595.0 KB (594986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d46b395c27ac3eb87ac760dbe7a0c25bd9e7140bd438760c4c202ce9cee5230`  
		Last Modified: Fri, 14 Nov 2025 19:34:56 GMT  
		Size: 44.3 KB (44306 bytes)  
		MIME: application/vnd.in-toto+json
