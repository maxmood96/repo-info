## `postgres:14-alpine`

```console
$ docker pull postgres@sha256:737a9ee1aa27ae45f69038e0be0415381469a2bd05af94122d830b4bb8c54fde
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

### `postgres:14-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:a9a8893c51d399bab4976abe439a26140020c57585666c9dc267b77837507f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108548699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c578ed49f6998c36c410ff232cdba50123167682e0ffb84eaeb4962be0e260b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:21:51 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Apr 2026 20:21:53 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:21:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 20:21:53 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 15 Apr 2026 20:21:53 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 20:21:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:21:53 GMT
ENV PG_MAJOR=14
# Wed, 15 Apr 2026 20:21:53 GMT
ENV PG_VERSION=14.22
# Wed, 15 Apr 2026 20:21:53 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Wed, 15 Apr 2026 20:21:53 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Apr 2026 20:23:51 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Apr 2026 20:23:51 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Apr 2026 20:23:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Apr 2026 20:23:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Apr 2026 20:23:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Apr 2026 20:23:51 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Apr 2026 20:23:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:23:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Apr 2026 20:23:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:23:51 GMT
STOPSIGNAL SIGINT
# Wed, 15 Apr 2026 20:23:51 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Apr 2026 20:23:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac4e45c6276fc7617f9926a53b6477e147ecb15e1281edccfe0daa4e00133d9`  
		Last Modified: Wed, 15 Apr 2026 20:24:06 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d6dc0feb9718759e81f599b2f4f046b6e48dbde813fd6a00de1f5052d02da1`  
		Last Modified: Wed, 15 Apr 2026 20:24:06 GMT  
		Size: 919.1 KB (919056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4faa1d0d63cfd15ff9d0430838f3eca500d4ab1bd5ff89b9355ee082b35266c`  
		Last Modified: Wed, 15 Apr 2026 20:24:06 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585db54b885ebc4bb1d2957fa26e51425be305b5549fe7e61b7cce08296319b5`  
		Last Modified: Wed, 15 Apr 2026 20:24:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634006cc3116d8c35968fda734d8a714cc5077c60b3077b07cb65436857bb67f`  
		Last Modified: Wed, 15 Apr 2026 20:24:10 GMT  
		Size: 103.7 MB (103748671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc442b3fff166cd3b5d6f12feb340356d4be615a98f41d0af175fac2e254d5a`  
		Last Modified: Wed, 15 Apr 2026 20:24:07 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba688a8edf083f3fc6a6346a8abc0573187ec298db3bacd9e7e1185d0fc2730`  
		Last Modified: Wed, 15 Apr 2026 20:24:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c09531377db006b68624b7c9bcec20850f00bdcf7855cb0b228daa4634c8e7`  
		Last Modified: Wed, 15 Apr 2026 20:24:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1f6061266eed5a5cd1ec5bb30c509ab1b50a356791a809bdfb19422e1a4455`  
		Last Modified: Wed, 15 Apr 2026 20:24:08 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0158a12d6ab6717713fbae4e258976df351e26166476a3ba68f69c0c8ee3ba`  
		Last Modified: Wed, 15 Apr 2026 20:24:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:c14965146ccea7c127113ca9fb351e0e05fb177dbf2aa41446ba5662848dcae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.2 KB (642179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63808d97314b066cc45d53728ddcd829be9cc946b367687f9c287a494f3dea64`

```dockerfile
```

-	Layers:
	-	`sha256:48f335bf3cba7f017f7bf8512c0e946f39aa47d1de206ef5cdf1e80bfb10a45a`  
		Last Modified: Wed, 15 Apr 2026 20:24:06 GMT  
		Size: 598.1 KB (598108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c70ca84542aafb368c0105f021c43ced4c0372c622eccc65ae940824b8a9d6c`  
		Last Modified: Wed, 15 Apr 2026 20:24:06 GMT  
		Size: 44.1 KB (44071 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:44ccd4be3977ce31b0fd8428779407f4f2e7b66ac0377cd860c55f51261fc7cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88051997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f44979333d35785b6b5b14e8afa9c394c54cfb401949c0950918e50dbd9fdb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:29:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Apr 2026 20:29:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:29:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 20:29:09 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 15 Apr 2026 20:29:09 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 20:29:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:29:09 GMT
ENV PG_MAJOR=14
# Wed, 15 Apr 2026 20:29:09 GMT
ENV PG_VERSION=14.22
# Wed, 15 Apr 2026 20:29:09 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Wed, 15 Apr 2026 20:29:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Apr 2026 20:31:54 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Apr 2026 20:31:54 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Apr 2026 20:31:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Apr 2026 20:31:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Apr 2026 20:31:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Apr 2026 20:31:54 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Apr 2026 20:31:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:31:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Apr 2026 20:31:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:31:55 GMT
STOPSIGNAL SIGINT
# Wed, 15 Apr 2026 20:31:55 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Apr 2026 20:31:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377e5ded654311851377a9267b2e560c09ddaf8141ac8f0acbcf93dba88f05c0`  
		Last Modified: Wed, 15 Apr 2026 20:32:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec989dc6a1e58083b280250c280a34f90bf20503e1441837f45909c56ea4cac`  
		Last Modified: Wed, 15 Apr 2026 20:32:05 GMT  
		Size: 887.1 KB (887110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56686a4ab5a694a30f0cb93b035d6373a95db3d1ac75e1b316655b1c4284573a`  
		Last Modified: Wed, 15 Apr 2026 20:32:05 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e22100e0c0b6b2d691cfee74673815a0daffbd51a54cbfa426ee070079a507e`  
		Last Modified: Wed, 15 Apr 2026 20:32:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9370d2fd3ef1f44088e1de8afec4c64207b3ebdc8c6c0e891e6b7a9412284f`  
		Last Modified: Wed, 15 Apr 2026 20:32:08 GMT  
		Size: 83.6 MB (83576251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c4b0b8d4c064f416292b029061eba6d21a5b94e998a7ca016612f74c0a7485`  
		Last Modified: Wed, 15 Apr 2026 20:32:06 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9618ddef915be137715ef9863b7c28f2ee50529cfadb87b5ac7e9a5fafbd0ecc`  
		Last Modified: Wed, 15 Apr 2026 20:32:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410fbe40998185f1a54cae0af5b178bed46860f8a47ace05af3a771c9f760fe9`  
		Last Modified: Wed, 15 Apr 2026 20:32:07 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a58ee71ce31e5223a3c8c143deb470f780b77e1aec6875c1dbc9f8c4a5d8150`  
		Last Modified: Wed, 15 Apr 2026 20:32:07 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e9c6b30bb654d90b0a68d8e8a69f483087641439659941d535ad47d7cc000c`  
		Last Modified: Wed, 15 Apr 2026 20:32:08 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:476132a35b5fb0263033850510989ae8b598f8d4177ae0c44819dc3525139a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 KB (44034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604542c278f1b25aa2b8c17e0eccb4be526c0df953d9fddaa991d104988e52c1`

```dockerfile
```

-	Layers:
	-	`sha256:15e74f2a2357ef566f6516717964e90e36c59222aacc3710fd953074124f14ae`  
		Last Modified: Wed, 15 Apr 2026 20:32:05 GMT  
		Size: 44.0 KB (44034 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:8c09e82814db4e19ece51602440d045f212e450ffcc3ba79c9ed0537df9323c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83323590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701f8233e1396b7b950a722ee69471dd075f7e535eac17fd5c8088a78603f7cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:28:59 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Apr 2026 20:29:02 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:29:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 20:29:02 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 15 Apr 2026 20:29:02 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 20:29:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:29:02 GMT
ENV PG_MAJOR=14
# Wed, 15 Apr 2026 20:29:02 GMT
ENV PG_VERSION=14.22
# Wed, 15 Apr 2026 20:29:02 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Wed, 15 Apr 2026 20:29:02 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Apr 2026 20:31:38 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Apr 2026 20:31:38 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Apr 2026 20:31:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Apr 2026 20:31:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Apr 2026 20:31:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Apr 2026 20:31:38 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Apr 2026 20:31:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:31:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Apr 2026 20:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:31:38 GMT
STOPSIGNAL SIGINT
# Wed, 15 Apr 2026 20:31:38 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Apr 2026 20:31:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02904390425dcbba6d09b56c8f9c62d47265ee17f669350290d3f85d11b8cbb`  
		Last Modified: Wed, 15 Apr 2026 20:31:50 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01dc2ee03a3229bfe6608669f1e8ccfab8a51a2fc52422fdb586a12eb1c11f3`  
		Last Modified: Wed, 15 Apr 2026 20:31:50 GMT  
		Size: 887.1 KB (887107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e8c4f1710c1a4fc64f4cd0ecfc6ef78b39e0f023213074a28a30807778bcc3`  
		Last Modified: Wed, 15 Apr 2026 20:31:50 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff74ff27825ee294d51d15de28ee90bf4ed9ed74bbfc132c70af720f823c890a`  
		Last Modified: Wed, 15 Apr 2026 20:31:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a66b4716fb2017f1f305a805d6543191a95df8a4de2e3bfdfaf1a83c7cef6a`  
		Last Modified: Wed, 15 Apr 2026 20:31:54 GMT  
		Size: 79.1 MB (79136576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e463cad66daf2b05346665f1791a1b1d0c6d1025626fdb40199ee7d98fcb60a8`  
		Last Modified: Wed, 15 Apr 2026 20:31:51 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d2b9124104f1d57bde2ff772f695e6c458dee05fad2a18bcc1fbd52ecc9d83`  
		Last Modified: Wed, 15 Apr 2026 20:31:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4c9743801310e92ece6edcba21591b531e6d900f7b496983de0bb0330f4fad`  
		Last Modified: Wed, 15 Apr 2026 20:31:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b2a8860703daeaaa9ad38a580232cf52a67a6dc253836648cecaa005ca834e`  
		Last Modified: Wed, 15 Apr 2026 20:31:53 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d311da5350e784a6ffac2799f444089023a068f36e585f597edff9cdadd7fd37`  
		Last Modified: Wed, 15 Apr 2026 20:31:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:d0d771d3ffd4e8a52da71eb58f89098fe307a4e6bcc405329095a342c1f5b3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.7 KB (641743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4851d3a77b2abb8f373c583b2375d88c9024593dfd8e0c8450fcb6dc9aa671bc`

```dockerfile
```

-	Layers:
	-	`sha256:d33e6cc59b5ff6e50449fd6e59b4b5bb22d519ba33dcae1af8a0639dc8b99472`  
		Last Modified: Wed, 15 Apr 2026 20:31:50 GMT  
		Size: 597.5 KB (597494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a82f0b3759af8e84e00eff0d2f278e7a340373ec0d4e8ca7136a7b0844d16a2`  
		Last Modified: Wed, 15 Apr 2026 20:31:50 GMT  
		Size: 44.2 KB (44249 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:4843742feee51b0409d8d830ad01ebf2dca9cd85f8a11f70ad01ce2212ea6187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106760712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33eaebd021d405f984976252a672af3912caf91cc28cadcd46e8f2d19f82da5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:21:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Apr 2026 20:21:25 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:21:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 20:21:25 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 15 Apr 2026 20:21:25 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 20:21:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:21:25 GMT
ENV PG_MAJOR=14
# Wed, 15 Apr 2026 20:21:25 GMT
ENV PG_VERSION=14.22
# Wed, 15 Apr 2026 20:21:25 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Wed, 15 Apr 2026 20:21:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Apr 2026 20:23:33 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Apr 2026 20:23:33 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Apr 2026 20:23:34 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Apr 2026 20:23:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Apr 2026 20:23:34 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Apr 2026 20:23:34 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Apr 2026 20:23:34 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:23:34 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Apr 2026 20:23:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:23:34 GMT
STOPSIGNAL SIGINT
# Wed, 15 Apr 2026 20:23:34 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Apr 2026 20:23:34 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd05185bdc58e87cfad51ef562e7471c2b323867c9d7faf96c159b7a52328c1d`  
		Last Modified: Wed, 15 Apr 2026 20:23:48 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e0a1c0f835b3500c36bff11c3accbf0e62a5a64b2a0c6314105eb3dc9377ff`  
		Last Modified: Wed, 15 Apr 2026 20:23:48 GMT  
		Size: 874.7 KB (874706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cfdc4aea25e5fc9ca0ef0d8af064549442383c12ce838bef8081630f2b2bd9`  
		Last Modified: Wed, 15 Apr 2026 20:23:48 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9ae3001aa9ecc1e9e3b0ea0940599cf96d86e625515ee47618ec0cf5e888d7`  
		Last Modified: Wed, 15 Apr 2026 20:23:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a8cf197512ce85822fccb61fa9004e507354fec849072d380aedacf6f6b208`  
		Last Modified: Wed, 15 Apr 2026 20:23:52 GMT  
		Size: 101.7 MB (101669354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e7cc0a2d2e3eb9df6e81dd2f186551cfe9e7a3b42105fcce7327f31c0209b4`  
		Last Modified: Wed, 15 Apr 2026 20:23:49 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cd23975f061d987a4e639cdfc00cb1b32fc0bf5a7ff5cca63eec947944e4d0`  
		Last Modified: Wed, 15 Apr 2026 20:23:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7b87e35f69b524572dd71826b173c1421c10c439cfcec6ffdcafc2a5c1aba8`  
		Last Modified: Wed, 15 Apr 2026 20:23:49 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b5b8d3312a62fa08ecdfe01ed72d8bcd46bf9b29f3796174d08fb86099a752`  
		Last Modified: Wed, 15 Apr 2026 20:23:51 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605eb5f56722e3f5b6b8945c444618fa05a63c71b6f32e517352789a5b8427b9`  
		Last Modified: Wed, 15 Apr 2026 20:23:51 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:f9b66fae5187118efd7e9d1674ca22216e64726d3cfec3279b3fb50b1479a2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.8 KB (641809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f14d86ba6ef2994160008f0703673e75bf3447ac861106879039d6fec6ceff`

```dockerfile
```

-	Layers:
	-	`sha256:b8f91957fd4ffdca6577eeebd59914985cbcc69c63838a620da884174df6eb6d`  
		Last Modified: Wed, 15 Apr 2026 20:23:48 GMT  
		Size: 597.5 KB (597514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51cd901212e579580390876c22ca9bacf68050335db5e79b858fe1ac75a224e5`  
		Last Modified: Wed, 15 Apr 2026 20:23:48 GMT  
		Size: 44.3 KB (44295 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine` - linux; 386

```console
$ docker pull postgres@sha256:4ed24ed548ac102543ed394b503686a6a130b05ea90a9d8e3a2d74b574412af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114577746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f8f5eb073f5753cbc670f63b5e1a0f9db095fc6bacc3086fa542a6e44e5319`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:25:10 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Apr 2026 22:25:13 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 22:25:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 22:25:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 15 Apr 2026 22:25:13 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 22:25:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 22:25:13 GMT
ENV PG_MAJOR=14
# Wed, 15 Apr 2026 22:25:13 GMT
ENV PG_VERSION=14.22
# Wed, 15 Apr 2026 22:25:13 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Wed, 15 Apr 2026 22:25:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Apr 2026 22:27:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Apr 2026 22:27:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Apr 2026 22:27:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Apr 2026 22:27:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Apr 2026 22:27:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Apr 2026 22:27:45 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Apr 2026 22:27:45 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:27:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Apr 2026 22:27:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 22:27:45 GMT
STOPSIGNAL SIGINT
# Wed, 15 Apr 2026 22:27:45 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Apr 2026 22:27:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72847f77b3917d64437c0452005928efc6beed619b18c991c94b94965e63397c`  
		Last Modified: Wed, 15 Apr 2026 22:28:01 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb326c876a247ae9b9efa232e488027e8092a5899e35282fabfe7ceee29589ad`  
		Last Modified: Wed, 15 Apr 2026 22:28:01 GMT  
		Size: 891.6 KB (891650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda6e0f6d1f37b378005c69fba33898006feb96fb4c8e56468b95b4a31d8b03f`  
		Last Modified: Wed, 15 Apr 2026 22:28:01 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358ba01f19140728ba0512d6da76104ac5d7827febf6f441a9e5bc803633fe0c`  
		Last Modified: Wed, 15 Apr 2026 22:28:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc511d15cd97a652bd5190db9e35c1702dfca5c327ab460db36407b88dd30784`  
		Last Modified: Wed, 15 Apr 2026 22:28:05 GMT  
		Size: 110.0 MB (109978869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ba1591bb97d022693df0c012a24a779def26bb91dbe04ced7fb7287f5b359f`  
		Last Modified: Wed, 15 Apr 2026 22:28:02 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76320a24843bd01d71935af4d035434a55271f009a82617ec59e2b3b9882cb9`  
		Last Modified: Wed, 15 Apr 2026 22:28:02 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bda10264dd9442460c840bafa9aa1243a62483622e77a67d1921c8197335ab3`  
		Last Modified: Wed, 15 Apr 2026 22:28:02 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acaa984c6d5ea110f1f60a35cffbc7f4ba553ae5be8198eb20c712857a99dee8`  
		Last Modified: Wed, 15 Apr 2026 22:28:03 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80abf0fb7f10d45be2a7232dced459996b8383ae750f291d7af1864315bbd58`  
		Last Modified: Wed, 15 Apr 2026 22:28:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:230a01acd9bcfa03208d097a55733e9bd76c67c39de27da3b4f4e6b98642baaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.1 KB (642104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023d0694ab69261eb985bbed624115c077d04ceaec2d39a3a77a6ecc4e49b1ad`

```dockerfile
```

-	Layers:
	-	`sha256:846748108d71a8fa344fc8669b1e141fc36f167940b7c060ea75e900fa7fd216`  
		Last Modified: Wed, 15 Apr 2026 22:28:01 GMT  
		Size: 598.1 KB (598083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cd1758ba9cdd0c57cbf5e1f74ea6a3754ff944bc5456593b76bc98041f6abaf`  
		Last Modified: Wed, 15 Apr 2026 22:28:01 GMT  
		Size: 44.0 KB (44021 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:6d65cb0026ecd7d6c698df899e9ef6b70fd75f72071321d7c96870a1a574394e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93399054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d36031d072e5414f39429683ad1eb4419f4b57a49f39cee00256e42ee449cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:55:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Apr 2026 20:55:24 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:55:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 21:00:23 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 15 Apr 2026 21:00:23 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 21:00:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 21:00:23 GMT
ENV PG_MAJOR=14
# Wed, 15 Apr 2026 21:00:23 GMT
ENV PG_VERSION=14.22
# Wed, 15 Apr 2026 21:00:23 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Wed, 15 Apr 2026 21:00:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Apr 2026 21:08:10 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Apr 2026 21:08:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Apr 2026 21:08:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Apr 2026 21:08:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Apr 2026 21:08:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Apr 2026 21:08:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Apr 2026 21:08:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:08:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Apr 2026 21:08:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:08:14 GMT
STOPSIGNAL SIGINT
# Wed, 15 Apr 2026 21:08:14 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Apr 2026 21:08:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9504179c89581170cbe497b214c2f97f01eae1cac5905e1d1fafdcf5bc01926d`  
		Last Modified: Wed, 15 Apr 2026 20:59:59 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a284924cfe2e8e2e82ff8309f349edbdfa04cfaa5de86e49b14e6cb75225a`  
		Last Modified: Wed, 15 Apr 2026 20:59:59 GMT  
		Size: 880.1 KB (880126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdbf69e74f8065c17f9aae6946c699680b19b0f5dac3b0eb9d86c6b4d150805`  
		Last Modified: Wed, 15 Apr 2026 21:04:25 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40505d0bc2ac480cc189bc63f3786b58510be6cd3ab7577555a65b6258920690`  
		Last Modified: Wed, 15 Apr 2026 21:04:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb42def7c828a2cefaa1de4239c824caa4cbfaedee8db85ae09ceb51c18cb47`  
		Last Modified: Wed, 15 Apr 2026 21:08:42 GMT  
		Size: 88.7 MB (88671214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6a8bbb75091c641b5448172848c0eefed944fde161969b39b89400b58407a5`  
		Last Modified: Wed, 15 Apr 2026 21:08:39 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8910090a6b676250442d4b436b08eb8119c19740d38c54bce38caa1f9525fc`  
		Last Modified: Wed, 15 Apr 2026 21:08:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e80a3a4503f76c9d9d7627c63bc6fea004d22911f49fdcc95c1d772cab5a287`  
		Last Modified: Wed, 15 Apr 2026 21:08:39 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708fe7c371484ff933ec12ba6e9e9d844961ccaa7d3cd7eac57ea04bd3a1b68d`  
		Last Modified: Wed, 15 Apr 2026 21:08:40 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886ea30e09249f124dcb6e2adc5533ca097ff25ae95c69750dcbd7497ebf5998`  
		Last Modified: Wed, 15 Apr 2026 21:08:41 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:2d6e3c4e3f84c907bc5fbafe793e0c268f1da59aa5ac6afae5eabc4d57103feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (639954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298a1fbfc4cc20c8ba49650b90b3af267dcebbf61a45607588c22b5ba8ced379`

```dockerfile
```

-	Layers:
	-	`sha256:cca94000d01d4c630ea19896ed775ab4937f24b7877f3e4fcad1cabb0279774d`  
		Last Modified: Wed, 15 Apr 2026 21:08:39 GMT  
		Size: 595.8 KB (595829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e52d239be1e16a345dc830232fff77922c0b93e198c11db92053306a7330ee8`  
		Last Modified: Wed, 15 Apr 2026 21:08:39 GMT  
		Size: 44.1 KB (44125 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:1bac27b6f332592de3bc854d48e4b4a5245c17a8f0cc8ce4eb7e35ec81ab6675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109464480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9796df80fba567691b50d3b4b3b0b0cb88069af8f8b8dfe621d08ed16a7d58ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 11:29:33 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 16 Apr 2026 11:29:45 GMT
ENV GOSU_VERSION=1.19
# Thu, 16 Apr 2026 11:29:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 16 Apr 2026 13:20:58 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 16 Apr 2026 13:20:58 GMT
ENV LANG=en_US.utf8
# Thu, 16 Apr 2026 13:20:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Apr 2026 13:20:59 GMT
ENV PG_MAJOR=14
# Thu, 16 Apr 2026 13:20:59 GMT
ENV PG_VERSION=14.22
# Thu, 16 Apr 2026 13:20:59 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Thu, 16 Apr 2026 13:20:59 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 16 Apr 2026 15:54:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 16 Apr 2026 15:54:45 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 16 Apr 2026 15:54:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 16 Apr 2026 15:54:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 16 Apr 2026 15:54:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 16 Apr 2026 15:54:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 16 Apr 2026 15:54:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 15:54:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 16 Apr 2026 15:54:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 15:54:46 GMT
STOPSIGNAL SIGINT
# Thu, 16 Apr 2026 15:54:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 16 Apr 2026 15:54:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c05352c3bc3bad2a071af544c560bfc66f25f632b9841754ed94c4abb19732`  
		Last Modified: Thu, 16 Apr 2026 12:22:58 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0841d6e8e03b3f5779ff0c2893e4e26e90895e6f4a7ec62726ad628be33e10e`  
		Last Modified: Thu, 16 Apr 2026 12:22:58 GMT  
		Size: 867.5 KB (867538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01640490039f18e0efc72dfc7e79e994ee5239169b238b30d21ba147a4d3d087`  
		Last Modified: Thu, 16 Apr 2026 14:14:12 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba82bcb214ae71de3d2b623be98402bc90b03aef6f555c7dd3f2d1a2a3676e2`  
		Last Modified: Thu, 16 Apr 2026 14:14:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c2852132fd7b92d77ae4256a477d20e2fbb5b61873942a1f4f26bc72648e5e`  
		Last Modified: Thu, 16 Apr 2026 15:57:47 GMT  
		Size: 105.0 MB (104992477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbb6ce77886aeba2f943d19bf4a454b1a7180f6aa59e83e0cba142ae8ef39e7`  
		Last Modified: Thu, 16 Apr 2026 15:57:32 GMT  
		Size: 9.2 KB (9214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72721799be3010480ed4883cfe0c55e92b6162805472fa68f602e3b4ea01dda`  
		Last Modified: Thu, 16 Apr 2026 15:57:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92935cab6e9cb32fb76c3195bf016c163d48291fb7ef86ec2c3402b1524ee90d`  
		Last Modified: Thu, 16 Apr 2026 15:57:32 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fc696b565a96bbcf6c0eea948c85dfcfa56d64e6c9e51ab29d2eedf060de43`  
		Last Modified: Thu, 16 Apr 2026 15:57:33 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9da275a96fd0caed57cb2959e94510166db8e7f59fa407d73c4d94cc5acb10d`  
		Last Modified: Thu, 16 Apr 2026 15:57:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:0c48728ac8c3e7df2e6a7136faeee6f3f539862976d0b1d3d10dea29a8476e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 KB (641618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f90a443bd6f62dc5343ec1feb5033f4b6f94648d0cc09c1db07fc6495d3759`

```dockerfile
```

-	Layers:
	-	`sha256:e232e15129a6e5a24b91b7a4d9bf391a23b40a999251994752c2c45ee5143d9f`  
		Last Modified: Thu, 16 Apr 2026 15:57:31 GMT  
		Size: 597.5 KB (597487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174184a13585852798aa5f1377e073b142ee939c39b20631b95e3b86242d22cc`  
		Last Modified: Thu, 16 Apr 2026 15:57:31 GMT  
		Size: 44.1 KB (44131 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:c28c8c36e6bcaa863a457de357b01fe07a4a5b8f815fad398788f8f8af1ce83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116677589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4df69fa0b1f64755d7dd316a5347dde4cf58aa12968827e5178342692656c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:32:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Apr 2026 20:32:28 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:32:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 20:37:51 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 15 Apr 2026 20:37:51 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 20:37:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:37:51 GMT
ENV PG_MAJOR=14
# Wed, 15 Apr 2026 20:37:51 GMT
ENV PG_VERSION=14.22
# Wed, 15 Apr 2026 20:37:51 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Wed, 15 Apr 2026 20:37:51 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Apr 2026 20:41:50 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Apr 2026 20:41:50 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Apr 2026 20:41:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Apr 2026 20:41:50 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Apr 2026 20:41:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Apr 2026 20:41:51 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Apr 2026 20:41:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:41:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Apr 2026 20:41:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:41:51 GMT
STOPSIGNAL SIGINT
# Wed, 15 Apr 2026 20:41:51 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Apr 2026 20:41:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c5ed854292088ad91fb5a623e51a3682312408cead42a22166de3fd8d1dc8a`  
		Last Modified: Wed, 15 Apr 2026 20:37:29 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ce62b957b857c08f679922ba4b91dc49057c951937637dd94b40a7fe8c5b81`  
		Last Modified: Wed, 15 Apr 2026 20:37:29 GMT  
		Size: 895.8 KB (895798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae20370d30162e578ddc4261332750d5420660a4b540ba6effcd03e08803223b`  
		Last Modified: Wed, 15 Apr 2026 20:42:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2957e716cf88c06abe669da7b50ef11d5b4dd8a2518ba299f5cc206a57082586`  
		Last Modified: Wed, 15 Apr 2026 20:42:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d314077ae85e6aaca9d7d27874337835053d80d57b6453153e4b049861043eb3`  
		Last Modified: Wed, 15 Apr 2026 20:42:18 GMT  
		Size: 112.0 MB (112038469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4ca017b083e36c20f2e1a80e8f37258d1ee0a55b5da0a6472d63662f73888d`  
		Last Modified: Wed, 15 Apr 2026 20:42:16 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5339a768d607e062c915dd3cb6a06d45742b8e2ca79b8d195202e970fc421030`  
		Last Modified: Wed, 15 Apr 2026 20:42:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c467eb9303242e61b0e1938c50bfb9386f2a83c879db3ccccb3ee53b5e38a3`  
		Last Modified: Wed, 15 Apr 2026 20:42:17 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641e0f6966afe2f6d44ea0a205260fea17791d7d6a97f2698350b2e74c19c6b9`  
		Last Modified: Wed, 15 Apr 2026 20:42:17 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f056e044821ddad51d6f2b288c5d56c680715f61d5f6753e0b9dbc72b16cb25`  
		Last Modified: Wed, 15 Apr 2026 20:42:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:5efefa1866b09619f3ef2757d60da6fda933e942d1ce36581900f6686cd2785c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.5 KB (641528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09714eaf9ebd4ddf8a23c37095647a6ea48492e3691735686a3791a01062b67f`

```dockerfile
```

-	Layers:
	-	`sha256:d5d56778e4c8e4fb1ef5ed934d295e2eb723ca287b69beaac538003ec6d743de`  
		Last Modified: Wed, 15 Apr 2026 20:42:16 GMT  
		Size: 597.5 KB (597457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d56c54c0fa6b6172a94589198bd3ad006b126282e5efb4fcbbfea7a72b288f5c`  
		Last Modified: Wed, 15 Apr 2026 20:42:16 GMT  
		Size: 44.1 KB (44071 bytes)  
		MIME: application/vnd.in-toto+json
