## `postgres:14-alpine3.23`

```console
$ docker pull postgres@sha256:c55392d0708cc0d4b00c8173b39ecf40aaf7e02e8f20d1a004ff9096cb2ab558
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

### `postgres:14-alpine3.23` - linux; amd64

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

### `postgres:14-alpine3.23` - unknown; unknown

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

### `postgres:14-alpine3.23` - linux; arm variant v6

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

### `postgres:14-alpine3.23` - unknown; unknown

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

### `postgres:14-alpine3.23` - linux; arm variant v7

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

### `postgres:14-alpine3.23` - unknown; unknown

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

### `postgres:14-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:321d83064cdb93992ffcd0e442ff08cd6d754af1bacecaa80bd14685e5c8da25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106759592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2820535dd39da3d7c9ab4453dafecb3f40a5d1392eb9a92b536a1213e4aeef1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:28:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:28:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:28:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:28:29 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:28:29 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:28:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:28:29 GMT
ENV PG_MAJOR=14
# Thu, 26 Feb 2026 19:28:29 GMT
ENV PG_VERSION=14.22
# Thu, 26 Feb 2026 19:28:29 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Thu, 26 Feb 2026 19:28:29 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:30:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:30:31 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:30:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:30:31 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:30:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:30:31 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:30:31 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:30:31 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:30:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:30:31 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:30:31 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:30:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954dfa73f01ed8125326b6f8a9335c78ae42425506e9502dbbfeccd9708f9163`  
		Last Modified: Thu, 26 Feb 2026 19:30:45 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c10b60474a2d7a74f3fa027272952a6cebcc187c51c3981ab10bea4b884e8e`  
		Last Modified: Thu, 26 Feb 2026 19:30:45 GMT  
		Size: 876.5 KB (876488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4212743af646f0561c6da8e99c02455e8b3162d7bffb0e3add2550137cab2924`  
		Last Modified: Thu, 26 Feb 2026 19:30:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293cf0e24c9ca711f33ccd94e41eeaef493813ad5a1799b0cb5b6e1817a44502`  
		Last Modified: Thu, 26 Feb 2026 19:30:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77380895aced3528426c65c84f2220c2d2f8c880ae383b6a4e0ff4ede3486b1`  
		Last Modified: Thu, 26 Feb 2026 19:30:49 GMT  
		Size: 101.7 MB (101669231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78edaf9aa2a54d6d2cfbda9ac06fe55ae87926433584465dd4ed6a6c59faa7a4`  
		Last Modified: Thu, 26 Feb 2026 19:30:47 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f3015ff1b1019cbbab5cefc8b153a4f4b023b597c61d97f70bcad050e8d647`  
		Last Modified: Thu, 26 Feb 2026 19:30:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0507f330873cfc1fb35e51cc953d0d9cae081f6e072d838e78eb5eaf1090c9`  
		Last Modified: Thu, 26 Feb 2026 19:30:47 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1be3d7350d19c243260178c9eff0503c855acd400005c1ee5b25fc18f89a490`  
		Last Modified: Thu, 26 Feb 2026 19:30:48 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d9dffcc8a54213ac2fb72e5f634f82c124f72ae677216d31ef6fcc1f794f1a`  
		Last Modified: Thu, 26 Feb 2026 19:30:48 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:98e7f679533e169b434b14fa1754a0699388a4c936b10fce808da4e7a8321e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.8 KB (641781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce88a5501ad4ace7bc051c088e6bce5554ebc17fb8def0360dd325fce9ee426e`

```dockerfile
```

-	Layers:
	-	`sha256:c257254810ada4c03fa5d6c7b8b7a4208b6e935cad3a27609de11e3add2d0ba2`  
		Last Modified: Thu, 26 Feb 2026 19:30:45 GMT  
		Size: 597.5 KB (597486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890687e1f25bbc9399221f8de17aff2cc5b870dc90c456d5da2a05c5a0b2b956`  
		Last Modified: Thu, 26 Feb 2026 19:30:45 GMT  
		Size: 44.3 KB (44295 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.23` - linux; 386

```console
$ docker pull postgres@sha256:f0de43c00937a78fa9b1b656cca113aa40254a44332dba3fdf85fe70b8d0c8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114576254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313db9559d5c67fb1d6b1ec33a0472841ca43b7d6704f1ee273eac9b9eb2467a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:25:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:25:44 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:25:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:25:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:25:44 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:25:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:25:44 GMT
ENV PG_MAJOR=14
# Thu, 26 Feb 2026 19:25:44 GMT
ENV PG_VERSION=14.22
# Thu, 26 Feb 2026 19:25:44 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Thu, 26 Feb 2026 19:25:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:28:02 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:28:02 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:28:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:28:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:28:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:28:02 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:28:02 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:28:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:28:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:28:02 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:28:02 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:28:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5164b89fa5dc76b39dc230f0ae0a8b6fcb74dd042d6e206a85d4a2e72010e6de`  
		Last Modified: Thu, 26 Feb 2026 19:28:17 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddae20b2b79c8caef511eb49908214204b94ae67dd3e15c0fa8914aa621f684`  
		Last Modified: Thu, 26 Feb 2026 19:28:17 GMT  
		Size: 893.3 KB (893256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14c6087cb95ee4d616b780d1eed7c698141ecb1328904732ac6c8c91abdf61b`  
		Last Modified: Thu, 26 Feb 2026 19:28:17 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dec41eec896bf215a8eba8c71616ba222494b290b58b37ed6bf66924250215`  
		Last Modified: Thu, 26 Feb 2026 19:28:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0084339341681d27133ceef5c0fcbb188b6098012da34827858de585e24a13a8`  
		Last Modified: Thu, 26 Feb 2026 19:28:21 GMT  
		Size: 110.0 MB (109979212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b2f56698e3ed362856a1d9387fa3d566538aec84ce4e7fb65a9e0b4e104384`  
		Last Modified: Thu, 26 Feb 2026 19:28:19 GMT  
		Size: 9.2 KB (9208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cbdfa1ba28b91cca86abfa12b1f1fb35237bfddd5654a9cd9c9e2b6890834b`  
		Last Modified: Thu, 26 Feb 2026 19:28:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efe592e582c9423e0d3a308879979bd64af295dd732fb0d03fda7c9ce4ef177`  
		Last Modified: Thu, 26 Feb 2026 19:28:19 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479abaf65445af440a18f12192c06b0422740f298613a896c032a53b563923f`  
		Last Modified: Thu, 26 Feb 2026 19:28:20 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b020a3636be48d96fadf93fd8ce2a97e96287509a20005d641920225af67c43`  
		Last Modified: Thu, 26 Feb 2026 19:28:20 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:8fabc4834363f68d40cc6b22efc141f8ab4d9d5936a4604786965776bcfe304d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.1 KB (642078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac6a77334b228fe61a818e350dce1a01b81ea07d8917d547a7f8cc145c01ab2`

```dockerfile
```

-	Layers:
	-	`sha256:63233073dba0aa169dd13aa6d74d93a5336309b2d661a76194607e6738a25d96`  
		Last Modified: Thu, 26 Feb 2026 19:28:17 GMT  
		Size: 598.1 KB (598055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da918c968aff0183cabf0b55878921a9bbb787cdda76a4ebb13c692a82270b1`  
		Last Modified: Thu, 26 Feb 2026 19:28:18 GMT  
		Size: 44.0 KB (44023 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.23` - linux; ppc64le

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

### `postgres:14-alpine3.23` - unknown; unknown

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

### `postgres:14-alpine3.23` - linux; riscv64

```console
$ docker pull postgres@sha256:4f7703bf27ef545d175fd31ec068d5d9768066be8e6329e1ccc9da676bd268c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109463727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeeff0d2f5b56c89888ce09bd60766488f97229b3733c47de26013f6dc756cf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 23:08:51 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 23:09:02 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 23:09:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Feb 2026 07:06:21 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 13 Feb 2026 07:06:21 GMT
ENV LANG=en_US.utf8
# Sat, 28 Feb 2026 10:27:04 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 28 Feb 2026 10:27:04 GMT
ENV PG_MAJOR=14
# Sat, 28 Feb 2026 10:27:04 GMT
ENV PG_VERSION=14.22
# Sat, 28 Feb 2026 10:27:04 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Sat, 28 Feb 2026 10:27:04 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 28 Feb 2026 14:35:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 28 Feb 2026 14:35:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 28 Feb 2026 14:35:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 28 Feb 2026 14:35:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 28 Feb 2026 14:35:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sat, 28 Feb 2026 14:35:10 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 28 Feb 2026 14:35:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 14:35:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 28 Feb 2026 14:35:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 14:35:10 GMT
STOPSIGNAL SIGINT
# Sat, 28 Feb 2026 14:35:10 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 28 Feb 2026 14:35:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4bf1089e3e4046b2263b0510bf148b29c663632753f3b12c015812638b3c1d`  
		Last Modified: Fri, 13 Feb 2026 00:02:06 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a22e9ae65cd8952ab5dcd13b337378c807b8c993fc757a882f6e64d9aa5fea`  
		Last Modified: Fri, 13 Feb 2026 00:02:06 GMT  
		Size: 868.9 KB (868941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c7e473c5c09f620cec1641eab266b62934fa5e0e6973c32870f53b87c923e8`  
		Last Modified: Fri, 13 Feb 2026 08:01:35 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd835550f29aa3e2cc22fe0488590a735c8fad8d8c9e2bf4946cd72ff8ecd187`  
		Last Modified: Sat, 28 Feb 2026 12:49:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4b9bd6f853974dcde717d5a4bea0ac037226abedb91226942422960df1d908`  
		Last Modified: Sat, 28 Feb 2026 14:38:11 GMT  
		Size: 105.0 MB (104992693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6680cd380ef7f30f7d0271c1fb6aa3975bc35272aed3a83e59eea038dd7e09f`  
		Last Modified: Sat, 28 Feb 2026 14:37:56 GMT  
		Size: 9.2 KB (9211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f506e82f2189738213afaceacb6f2ea93c3220810cc485494aa25a71cc9c7b9e`  
		Last Modified: Sat, 28 Feb 2026 14:37:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de6be14cf0b005102da7e05d30ef62eee60be6011a8bb31ad827014222c5bd1`  
		Last Modified: Sat, 28 Feb 2026 14:37:56 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ac980ca77f08f6ebf6008be3067a4d7911f5d474e1654d9a8781b82fbba105`  
		Last Modified: Sat, 28 Feb 2026 14:37:57 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf85d46f44cbab07cd84ae8993a793ffb19f2d85396e885e72a28dc2835244d4`  
		Last Modified: Sat, 28 Feb 2026 14:37:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:f54fc878bbe56582c09da66ab2176a3676c3b1b785f77e98be3c230f844e35fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 KB (641589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c4861dd232aaa9023ba73bb8267bb824ab68245f4fa0e665eb0ce1ae2a5f6e`

```dockerfile
```

-	Layers:
	-	`sha256:11a620e2cec60a0a384ab93fe0ba4391d89966e97d63c2659d625d4d5f171aec`  
		Last Modified: Sat, 28 Feb 2026 14:37:56 GMT  
		Size: 597.5 KB (597459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbee63e33992c49f0eea0476d0475c203a411bca51c975638a92cf13197a908c`  
		Last Modified: Sat, 28 Feb 2026 14:37:56 GMT  
		Size: 44.1 KB (44130 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.23` - linux; s390x

```console
$ docker pull postgres@sha256:7e5a0ab34a7bee7029cf49959a90a03400863510f938b04d6facd47d7ea7a455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116677894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca671f94f7f84e18282a95d8a5014eef2cfb1ab08b00dc34fe2b9a60524280a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:14:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:14:55 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:59:34 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:59:34 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:59:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:59:34 GMT
ENV PG_MAJOR=14
# Thu, 26 Feb 2026 19:59:34 GMT
ENV PG_VERSION=14.22
# Thu, 26 Feb 2026 19:59:34 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Thu, 26 Feb 2026 19:59:34 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 20:09:58 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 20:09:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 20:10:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 20:10:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 20:10:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 20:10:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 20:10:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6390f8026daaba6b4a0ba5ea908c8dc6349dd04610c8042fed5bdeb177e261`  
		Last Modified: Thu, 26 Feb 2026 19:19:15 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20d057a6a7a5332d1a6ec5069dcaee3c83e9a8d5596baf55423cd8546a0408d`  
		Last Modified: Thu, 26 Feb 2026 19:19:15 GMT  
		Size: 897.4 KB (897425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ed007f17e76310eb0dc0655c01e2c2a26235076fd16d1c913db839375a5bb2`  
		Last Modified: Thu, 26 Feb 2026 20:04:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857f6386ecadccec6c01fd0e28be3b682b5f2fed27bd7287c85d28fac39f861e`  
		Last Modified: Thu, 26 Feb 2026 20:04:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2757df9985ce65b9bd37e8b1315ee501d239d3ab23cddfde40516975db60ea`  
		Last Modified: Thu, 26 Feb 2026 20:10:34 GMT  
		Size: 112.0 MB (112038343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecf320894582077b5364184a0858bf5eeead34afccc4902e7a85026841a1de4`  
		Last Modified: Thu, 26 Feb 2026 20:10:32 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067c210127b27f84b94c4f5858d30d7c18afc6e53d5225a6b208fb2f006212a6`  
		Last Modified: Thu, 26 Feb 2026 20:10:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561c17b7ceb754d6f5ed04d012bb07d6539fcd22aa7263c3a418a5cd0def78e9`  
		Last Modified: Thu, 26 Feb 2026 20:10:31 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb1ba43289d04b857a36a706806d4cbbb8a32cfb166cdb7b199096a4e8a11d9`  
		Last Modified: Thu, 26 Feb 2026 20:10:33 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c17a1e501c5d3c2268e48c2f66088196669d55216a520471113613ae048d7f`  
		Last Modified: Thu, 26 Feb 2026 20:10:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:8bf3682556d31d6fd1ac2a72a864c4c5156bc7d0acc92cb565a825b77d8815a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.5 KB (641499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc67f5d6cab06fd0f360c5b6581eae3075b5336d78890cf0b9beb6d96c0de02`

```dockerfile
```

-	Layers:
	-	`sha256:ac1af0976da455b48b1a6c769d757472ed5c4d5f5a28ed07caf5523b5a52f7e8`  
		Last Modified: Thu, 26 Feb 2026 20:10:31 GMT  
		Size: 597.4 KB (597429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:404839c7590f70c1352986719bda7b9f71b5a30b76af52cd12e18679b7358a69`  
		Last Modified: Thu, 26 Feb 2026 20:10:32 GMT  
		Size: 44.1 KB (44070 bytes)  
		MIME: application/vnd.in-toto+json
