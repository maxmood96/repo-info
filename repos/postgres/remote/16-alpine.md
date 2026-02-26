## `postgres:16-alpine`

```console
$ docker pull postgres@sha256:b7587f3cb74f4f4b2a4f9d67f052edbf95eb93f4fec7c5ada3792546caaf7383
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

### `postgres:16-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:60b180625695e90b6e450405d5f0bcb74bc8c52c65d1cd11aeb3da46cac06dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109974689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108b27c919e6e7bc124350fb265deea9adac58e118eade428c6d1ad44b90debe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:25:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:25:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:25:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:27:49 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:27:49 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:27:49 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:27:49 GMT
ENV PG_MAJOR=16
# Thu, 26 Feb 2026 19:27:49 GMT
ENV PG_VERSION=16.13
# Thu, 26 Feb 2026 19:27:49 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Thu, 26 Feb 2026 19:27:49 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:29:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:29:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:29:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:29:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:29:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:29:56 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:29:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:29:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:29:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:29:56 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:29:56 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:29:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf295aa7a64cc10d3fd90a45852e84698ec47f2e92520fb998849df6910405c7`  
		Last Modified: Thu, 26 Feb 2026 19:27:39 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b36925b35104b27973d3cfe252ab78a77c21068863402468cb7dba8d8e91109`  
		Last Modified: Thu, 26 Feb 2026 19:27:40 GMT  
		Size: 922.9 KB (922922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850791607874d1c928ff4304a305188f179c5c588c885973a7ccb32d51d6e6f`  
		Last Modified: Thu, 26 Feb 2026 19:30:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc66e2c13be500cf88269ccd9a5d92bba5c124aa6ecb54c839fd5a74ffbbb47e`  
		Last Modified: Thu, 26 Feb 2026 19:30:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb0a9f61bdfa2e3f5a5f4da3bf87aadbe9825329ecec6bc3c05360ceddeee16`  
		Last Modified: Thu, 26 Feb 2026 19:30:13 GMT  
		Size: 105.2 MB (105172749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0210f91556cdadc6cd56501371d7d16c704302f8aa4afa5d41477eb38b99812`  
		Last Modified: Thu, 26 Feb 2026 19:30:11 GMT  
		Size: 9.6 KB (9617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d513847b8a7646505b10580f412411282b44b9b7c1974a96cb4e93001a6c459c`  
		Last Modified: Thu, 26 Feb 2026 19:30:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffbff44edafec4dbf8192cc2e75332188cfa9f992160ad7b1cf59f3d6d4e8a7`  
		Last Modified: Thu, 26 Feb 2026 19:30:12 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ea68590de1266d8c1945919c97389d55ed233df091227033b16a084ee69f0d`  
		Last Modified: Thu, 26 Feb 2026 19:30:12 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8dcc9ff6fd14be05d8afdc74d1c6aefa903a05ea51bb8a790410bce6060b2e`  
		Last Modified: Thu, 26 Feb 2026 19:30:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:19420411bc2b75747c7dc91cd11439fd637a4a7a1d587fa549be7abb23263508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c4ee79ead5a7b110b6aec9759a00e00437c9697055b42910d8dd2e0882c290`

```dockerfile
```

-	Layers:
	-	`sha256:233faecbc10ffcaf1cac5021f747196c7548b23b67ca55c0e811892a186e72be`  
		Last Modified: Thu, 26 Feb 2026 19:30:11 GMT  
		Size: 598.1 KB (598080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17a9c35415d58e26446186f3246d48379f452884d5be734dcf04926abae6996d`  
		Last Modified: Thu, 26 Feb 2026 19:30:10 GMT  
		Size: 44.3 KB (44306 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:698411232d7caa8a8f275a89d556e6abc6e9dfc7e0662699b5d57ba5bcf7dd90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89404458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35afc8af612ff135815a82eb118b4bb605a85189c5485a3eeab223e3a9dc7e95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:16:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:16:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:16:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:16:21 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:16:21 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:16:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:16:21 GMT
ENV PG_MAJOR=16
# Thu, 26 Feb 2026 19:16:21 GMT
ENV PG_VERSION=16.13
# Thu, 26 Feb 2026 19:16:21 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Thu, 26 Feb 2026 19:16:21 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:19:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:19:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:19:15 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:19:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:19:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:19:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:19:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:19:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:19:16 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:19:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:19:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97a36decbef7bd88a426040b3c5f4f764a1c29860da58e58eb3f33bc015b7ae`  
		Last Modified: Thu, 26 Feb 2026 19:19:28 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aecaa5edb7739e5531d5a3c10868cdb88d81a81b58a8848ae75ee37181cde5`  
		Last Modified: Thu, 26 Feb 2026 19:19:27 GMT  
		Size: 889.5 KB (889471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13423d67b2d658beeae002d6308308448b5d96eefc807816bdc95fd69b53855`  
		Last Modified: Thu, 26 Feb 2026 19:19:27 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424ff99b73495efe2c838e14bb8d34d725f19980340bc4f1bc35d94ea257b471`  
		Last Modified: Thu, 26 Feb 2026 19:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8083d890eb50c9ef0d0714533d6ca1f7a6d5580d50f3412035ba512dd9402ebb`  
		Last Modified: Thu, 26 Feb 2026 19:19:31 GMT  
		Size: 84.9 MB (84927966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98a2551b51122c3ac772fe781168bce8a083386b88ea6d95fe2f09307166074`  
		Last Modified: Thu, 26 Feb 2026 19:19:29 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a516264622f23d4eae37918a451705700f55d9f2eae299934d405121c561b663`  
		Last Modified: Thu, 26 Feb 2026 19:19:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc89deb1323f7c9daeeb15079bb1b55784daf53bb3fef71ccd2b67cce6e75ea8`  
		Last Modified: Thu, 26 Feb 2026 19:19:29 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8ddbbd4aadc0da317b1a093ac068cb299a32bce97bbe01140a3b06ffa721d0`  
		Last Modified: Thu, 26 Feb 2026 19:19:30 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b4232fe1fd503901144b5fd17ac1108bd9d4070fda350ea629d24b27aa671`  
		Last Modified: Thu, 26 Feb 2026 19:19:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:9a936694d56c0942bc7916b0a35d06d1425b29866999d6fc152e004cb583bffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 KB (44266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f35e3052b6f5396e48232d04d5d93aa7bebb934b647b9686f736459df97c86c`

```dockerfile
```

-	Layers:
	-	`sha256:bec70f9307d3e2014f78326ea02254ba5ad40763a8251a66a7bd5741623dfc2b`  
		Last Modified: Thu, 26 Feb 2026 19:19:27 GMT  
		Size: 44.3 KB (44266 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:6ba5f528786dcc296ab4b6d70c1699d224659583e6df320ee1c39e33b4111820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84641251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5a779c8b74a93c872fda5ed2e86816ebbfaabfb2b09d0041caac86318f2830`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:16:11 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:16:15 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:16:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:37:33 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:37:33 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:37:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:37:33 GMT
ENV PG_MAJOR=16
# Thu, 26 Feb 2026 19:37:33 GMT
ENV PG_VERSION=16.13
# Thu, 26 Feb 2026 19:37:33 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Thu, 26 Feb 2026 19:37:33 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:40:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:40:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:40:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:40:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:40:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:40:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:40:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:40:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:40:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:40:18 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:40:18 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:40:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad4001526fdff3d2d09a6e6e23e4e6340491f0b7e20bcb8e1093c1570876624`  
		Last Modified: Thu, 26 Feb 2026 19:19:13 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba14f83bbfc8d279e5118315290767edfa466091e98f2af7341ba2b0b72757fc`  
		Last Modified: Thu, 26 Feb 2026 19:19:13 GMT  
		Size: 889.5 KB (889515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4370adbf5520ba8fcc03949b461a57f73aca454fd2303b1213f2213d3ac1a2b`  
		Last Modified: Thu, 26 Feb 2026 19:40:29 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e44a87bd7587a7c42a448200a86365168e3f767714d9b0e98917d26a759c56`  
		Last Modified: Thu, 26 Feb 2026 19:40:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2c9310c2d3ab40a549e9be5becaed2d75db68efc0638b46ffa9f606dfdd66a`  
		Last Modified: Thu, 26 Feb 2026 19:40:31 GMT  
		Size: 80.5 MB (80452810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cc81e5461679f5c6e13e77b7454dba8c9ded78be833019bf74e8c340388caf`  
		Last Modified: Thu, 26 Feb 2026 19:40:29 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72584b6d5690f8a86b5f0cae709a555c3111d31f4531724fa12b2e56df5e49e`  
		Last Modified: Thu, 26 Feb 2026 19:40:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b65507341c2d4da28881f52f9bbcb26436541de21e8a64f474d7986fb0753bf`  
		Last Modified: Thu, 26 Feb 2026 19:40:30 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559278b601d0358d8200663e1e6f35165b88b2e4f80f51648415e5b1d223f3ef`  
		Last Modified: Thu, 26 Feb 2026 19:40:30 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24020ca08e4659dd48e2d13cb83a5df62c7e122cbf8a2424517f912a7795ea0`  
		Last Modified: Thu, 26 Feb 2026 19:40:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:641634e2b3209d88827db17fc6a13452e3cca15cc9cd1029737b0e72152b25ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.0 KB (641950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34585831dedd384e69323069cf69a62a6d53aff52cd58e85dbf31f49f6c74d2f`

```dockerfile
```

-	Layers:
	-	`sha256:f70b09b812b7b806d05702584db5a99705676967e885508713c92ba4871858ad`  
		Last Modified: Thu, 26 Feb 2026 19:40:29 GMT  
		Size: 597.5 KB (597466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f4a9c296230880ebd806bdd95d7372ec8ce0be43849d892384ff739f8799fd0`  
		Last Modified: Thu, 26 Feb 2026 19:40:29 GMT  
		Size: 44.5 KB (44484 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:d4e7bbd53503d420c248ad3039898876b7971bf5e51a6eb2f0b8c00ae8e718d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108168779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7a666480d0a8efb29f3c7876fc612147be6a37f071b74a3131248d3818ae3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:21:35 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:21:38 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:21:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:25:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:25:39 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:25:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:25:39 GMT
ENV PG_MAJOR=16
# Thu, 26 Feb 2026 19:25:39 GMT
ENV PG_VERSION=16.13
# Thu, 26 Feb 2026 19:25:39 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Thu, 26 Feb 2026 19:25:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:27:51 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:27:51 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:27:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:27:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:27:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:27:51 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:27:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:27:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:27:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:27:51 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:27:51 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:27:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79adb56125dd8f7feb6afc78fc07ede4c98caa32fd4e6b41f47600828da1bfc9`  
		Last Modified: Thu, 26 Feb 2026 19:24:19 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916f1ad40c1291c13adbbc451c47990f7743902c9e8899400d33a2d3ec383074`  
		Last Modified: Thu, 26 Feb 2026 19:24:19 GMT  
		Size: 876.5 KB (876493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d85c14803ffc130e481a585ec92b28b8afcfeeacf79c91ffd9bd44a007caf1e`  
		Last Modified: Thu, 26 Feb 2026 19:28:05 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58563aacf9ee3a728efadf3a3ae88bf7c6ecceb5276c67e10f84605286ec3dac`  
		Last Modified: Thu, 26 Feb 2026 19:28:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8f3437ce1b0dcaaa3c94cd468884c9b02d24b2b564a251c6c28772423d3b6c`  
		Last Modified: Thu, 26 Feb 2026 19:28:09 GMT  
		Size: 103.1 MB (103077994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7419a9c52e02a7b996ee048069ec4de899c6131d97d8faf405ce63ab3b50d0a4`  
		Last Modified: Thu, 26 Feb 2026 19:28:05 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b582240ca8c784720f7dd45d917ca72b857546316bf2b420ebb9dd1bf4c297`  
		Last Modified: Thu, 26 Feb 2026 19:28:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4328d592a54b7e382f9b78b8f56d44b686ab1b761c68abdcd01f6975aa14020f`  
		Last Modified: Thu, 26 Feb 2026 19:28:07 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bb20b6ce3efe64e83ecec646adb794188d7698295946e29fe2b6765176dd5f`  
		Last Modified: Thu, 26 Feb 2026 19:28:07 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06d9135182e824407f477c02bc039c7eb6845080abefdda56aa464b3ecbba96`  
		Last Modified: Thu, 26 Feb 2026 19:28:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:cd266d39f50002ff3287145fdee6d0d803eabd703fa1f178c11565d2ec9f5e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.0 KB (642016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739c192ca50becf84f76587c585c6034c72daa25167c57661298a764b3e4c567`

```dockerfile
```

-	Layers:
	-	`sha256:7efa8dcabfcab7300245d0bebeb67cb87ff0a75c50b9486339026910f68a8d49`  
		Last Modified: Thu, 26 Feb 2026 19:28:06 GMT  
		Size: 597.5 KB (597486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2e8f55ae2fa0afc6507795f52a00afbf36f02a965268870bbb05d390a489b55`  
		Last Modified: Thu, 26 Feb 2026 19:28:05 GMT  
		Size: 44.5 KB (44530 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; 386

```console
$ docker pull postgres@sha256:1f1bd3075d7d5bab1a72d24ce18dee7196c0072785de6915d1d13344faf76f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116004567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c4de9e8b8889ad2de3d760652a659557285d7058cc107ec8ccc73d14c41d86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:19:42 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:19:44 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:19:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:19:45 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:19:45 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:19:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:19:45 GMT
ENV PG_MAJOR=16
# Thu, 26 Feb 2026 19:19:45 GMT
ENV PG_VERSION=16.13
# Thu, 26 Feb 2026 19:19:45 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Thu, 26 Feb 2026 19:19:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:22:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:22:04 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:22:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:22:04 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:22:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:22:04 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:22:04 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:22:04 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:22:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:22:04 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:22:04 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:22:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca3f36e628194c5db212861a0456aa02929490f2a8fccda365622dbb55114f7`  
		Last Modified: Thu, 26 Feb 2026 19:22:19 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80279213af2ed085d7c6bea433f20529bdbe95e9a409ffd805fb8e8de6fed5f`  
		Last Modified: Thu, 26 Feb 2026 19:22:19 GMT  
		Size: 893.3 KB (893259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2b21d0d4515ea3aaf3f3c42ed1cdef13f035d4101b98317f62577213f9e73e`  
		Last Modified: Thu, 26 Feb 2026 19:22:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9273fdea5edb21fed72de1e7e7a42ff4795df5ce241e74e05da03e3c83e6a104`  
		Last Modified: Thu, 26 Feb 2026 19:22:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b77884bea3e26045465a25f71b1d0dbadfbec4cedc1ad477a3522cd5d35cf59`  
		Last Modified: Thu, 26 Feb 2026 19:22:23 GMT  
		Size: 111.4 MB (111407107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0c9825e6779af77c27686c81d935999f458fd4f68254a1de0afee82b240d95`  
		Last Modified: Thu, 26 Feb 2026 19:22:20 GMT  
		Size: 9.6 KB (9621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420c4b2756a68bfbdf1acb2edec0c26512b2ccb11336a60f77d0ee6a2b6ad5ef`  
		Last Modified: Thu, 26 Feb 2026 19:22:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f606bea02009e32db3024790ec03e21019958476821ecb9ca929b015cc5beb`  
		Last Modified: Thu, 26 Feb 2026 19:22:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a1776431e81e5d911c89e4d1f5cb878ae1528cfb852e744b1775033ed3782c`  
		Last Modified: Thu, 26 Feb 2026 19:22:21 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a821b84ea01bfe387119b0c38aa899a229511d7ac8e3cc338d626c3b88fd4a76`  
		Last Modified: Thu, 26 Feb 2026 19:22:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:44461570478576cc29b9dad93a0fc0b24f9cae4268e8c53816e032605fff6292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.3 KB (642312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d276b4d723b41a70dc557488b82773d6e02d8665d3da9c7b65739c91e1a5bfd`

```dockerfile
```

-	Layers:
	-	`sha256:1230df64794b55b7dc3f858a5e50c97f917498cc03e185030e8858084a76dbb2`  
		Last Modified: Thu, 26 Feb 2026 19:22:19 GMT  
		Size: 598.1 KB (598055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca9a1b2aa066a474cd3ccda625a5642cd8275708afec69995d3880694aeef4c1`  
		Last Modified: Thu, 26 Feb 2026 19:22:19 GMT  
		Size: 44.3 KB (44257 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:971c0643f7078b889d9285f98b12af3f75efca07e425b82b52ed3ce713ed5c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94898145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1090aeb099c497265e052baf60f859e4422024a9259a07d7dce7bfb333db6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:05:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:05:44 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:05:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:20:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 12 Feb 2026 21:20:13 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:28:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:28:57 GMT
ENV PG_MAJOR=16
# Thu, 26 Feb 2026 19:28:57 GMT
ENV PG_VERSION=16.13
# Thu, 26 Feb 2026 19:28:57 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Thu, 26 Feb 2026 19:28:57 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:32:35 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:32:36 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:32:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:32:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:32:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:32:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:32:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:32:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:32:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:32:38 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:32:38 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:32:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3303791000843bb87e4139ec69d0072bf49042341568a87e31e34fee9bb6b8d`  
		Last Modified: Thu, 12 Feb 2026 21:10:41 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b84c177f4fdd062892cae0bf053756f85b594952f273a772df42fab740e47f3`  
		Last Modified: Thu, 12 Feb 2026 21:10:41 GMT  
		Size: 881.5 KB (881516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5c2b538dfb06dace37986f411966827fb126b105e5c672fd572c190a045e4a`  
		Last Modified: Thu, 12 Feb 2026 21:24:34 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3241c041067e4c8b22d27ae7ac4f8a78e972ef5a3691ba9d5c65bca8e91db23b`  
		Last Modified: Thu, 26 Feb 2026 19:33:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895c3a96d144d69fdd76000caaf1b1cbc1b272ed1c498987d8333f8734aa47b6`  
		Last Modified: Thu, 26 Feb 2026 19:33:15 GMT  
		Size: 90.2 MB (90169771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f162f9fb45819dbb5042b7b772634c8e41ace8a28d21996f261d5834b60250`  
		Last Modified: Thu, 26 Feb 2026 19:33:13 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72142b8ecb58d73247698e7d6f4ae012a485b90952589cff00eecdcd0c6f0a48`  
		Last Modified: Thu, 26 Feb 2026 19:33:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8206c5934f69dfb25b7e2e0be4302ab1b069ca71de2a8f372bc55a855d9042`  
		Last Modified: Thu, 26 Feb 2026 19:33:14 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f259b22397f22a69ddf8d05b6d9e9ebcbd9388b83f57265dd9996600f37c0cf0`  
		Last Modified: Thu, 26 Feb 2026 19:33:14 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4147d5e34aa74519bfeb945e144d1ee57d617ad058c6ae6a84c36977aebcb5`  
		Last Modified: Thu, 26 Feb 2026 19:33:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:b268f45354aaac79ba734f4468ec2ceb99883fd45af2568c6155a7501c80374f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b2bfaee27e254d573b70dfb3eb8127e2bef654bacadc28e166b658d973baf9`

```dockerfile
```

-	Layers:
	-	`sha256:3be696960ff8b141279fda58e541599d11b5136f3cfa107e5f3595136e311760`  
		Last Modified: Thu, 26 Feb 2026 19:33:13 GMT  
		Size: 595.8 KB (595801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3de9b7d8255db3f2e19b50ce945c577eb5705beacd404eebbfc3f2ae5b96d7c`  
		Last Modified: Thu, 26 Feb 2026 19:33:12 GMT  
		Size: 44.4 KB (44360 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:c6e796f56abda78fcc765158ee8ee8443503bcc1932b35fc19b4ea9bdb5fe5ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (111018688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a6c843c09e36cd4c2d9b8c6b5330ea36036ab2ad82ceaa84f278b683433b3d`
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
# Fri, 13 Feb 2026 07:06:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 13 Feb 2026 07:06:21 GMT
ENV PG_MAJOR=16
# Fri, 13 Feb 2026 07:06:21 GMT
ENV PG_VERSION=16.12
# Fri, 13 Feb 2026 07:06:21 GMT
ENV PG_SHA256=b253ee949303ef5df00e24002600da4fb37e5ccfafa78718c6ea6a936b4d97f1
# Fri, 13 Feb 2026 07:06:21 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 13 Feb 2026 07:58:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 13 Feb 2026 07:58:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 13 Feb 2026 07:58:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 13 Feb 2026 07:58:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 13 Feb 2026 07:58:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 13 Feb 2026 07:58:46 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 13 Feb 2026 07:58:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 07:58:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 13 Feb 2026 07:58:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Feb 2026 07:58:47 GMT
STOPSIGNAL SIGINT
# Fri, 13 Feb 2026 07:58:47 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 13 Feb 2026 07:58:47 GMT
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
	-	`sha256:26cd7750064e6edef205cbd62fcb323dcff28fb079e21fbe3b8d66424ff940a6`  
		Last Modified: Fri, 13 Feb 2026 08:01:35 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6ae66b6ea53fa052235ff582d7a5a3a7f9846108317ee07326644dbdd379ec`  
		Last Modified: Fri, 13 Feb 2026 08:01:51 GMT  
		Size: 106.5 MB (106547238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83d73aeb907f08779bb535826248db599ed2852629c0cabddd49e853873730a`  
		Last Modified: Fri, 13 Feb 2026 08:01:35 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71104233247d5554e1b86f7b973f3fe532b96aa70628b576324e4a6412dbf1c3`  
		Last Modified: Fri, 13 Feb 2026 08:01:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a5aa5c877f29e8cbbf16acbca2eccb9b0a60063608a3740aeb2c086287fd91`  
		Last Modified: Fri, 13 Feb 2026 08:01:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b25f395124a21481c99937f818fe2807265d59508e23ad85def2a37b3dac10`  
		Last Modified: Fri, 13 Feb 2026 08:01:37 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b46ccee0875ae5454c776ceee4fba7343f6465eaf069afaee546994b580c61`  
		Last Modified: Fri, 13 Feb 2026 08:01:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:fd126566579fa2e4f5dbaf978140906b4784dc6b2d13eba00d91d6687c4055a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.8 KB (641825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a03c09b77238d49a2bbc1826190294534e7d69a382f3e4c0814c2bad26a58aa`

```dockerfile
```

-	Layers:
	-	`sha256:4bfe7415eac90915c0ff60854b2d28559e3369c0716a4ebdfdbc52a489ffcc74`  
		Last Modified: Fri, 13 Feb 2026 08:01:35 GMT  
		Size: 597.5 KB (597459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a674af3a4b2a964443243e71fd846d9d05c5ba6c41d0596acba65e60f6ebd38f`  
		Last Modified: Fri, 13 Feb 2026 08:01:35 GMT  
		Size: 44.4 KB (44366 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:f49c8fa7cf587f02f40ee99b2c9acaca76453dfce86dbd733ea7a2213fff358e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118095048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9552ba436e9377b26d1d25b694429f20d804cf84baa6c7445c11b67b743dabcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 23:34:49 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:40:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:40:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:40:26 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:40:26 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:40:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:40:27 GMT
ENV PG_MAJOR=16
# Thu, 26 Feb 2026 19:40:27 GMT
ENV PG_VERSION=16.13
# Thu, 26 Feb 2026 19:40:27 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Thu, 26 Feb 2026 19:40:27 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:44:29 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:44:31 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:44:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:44:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:44:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:44:33 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:44:34 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:44:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:44:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:44:36 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:44:36 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:44:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32e9b7742fe584659e12027c33c400a4177f291e191753d48596ef84ac6ec61`  
		Last Modified: Wed, 18 Feb 2026 23:39:16 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb3bc9055ac62b0b138d240b97e4cfb0d0656a56953b9cf1c00d287a697bad2`  
		Last Modified: Thu, 26 Feb 2026 19:45:19 GMT  
		Size: 897.4 KB (897426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17785b0e67ca21a84f365ecae8b55dc3fa0bb71f95e5d4ca3476229ee869e67c`  
		Last Modified: Thu, 26 Feb 2026 19:45:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6f63b4d999cd25657ca03f69a8292f4c5c9d5233a327cd1df29148c43820a9`  
		Last Modified: Thu, 26 Feb 2026 19:45:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03458acedf88f38f5379b9ad09c9b6b6524f5b966ad93ffa9d8e4e8defde806e`  
		Last Modified: Thu, 26 Feb 2026 19:45:24 GMT  
		Size: 113.5 MB (113455083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70884288a5259b1dbda59bd9f404015a8c355c1517680a6c4ef80957dc96adf`  
		Last Modified: Thu, 26 Feb 2026 19:45:21 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7893c3ff90e437da82ffaf4e96df3eacdfc88f78756495a888a45fb31e2970`  
		Last Modified: Thu, 26 Feb 2026 19:45:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6b53a5d1eae986c64283d3371329760662ea2263efb8a462fd0e6859c328b4`  
		Last Modified: Thu, 26 Feb 2026 19:45:21 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43ccbcfe32a3c78004d2469d16382c34c43816a7a5198b8192b23d85bb1a3d7`  
		Last Modified: Thu, 26 Feb 2026 19:45:22 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ce9f1f99c4ec9d30e8408f46006c61ff9a7d6b16c6daac35a5805903dfccf3`  
		Last Modified: Thu, 26 Feb 2026 19:45:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:187ff538ff38c958900f080fae6e75df8196e9a81f285d40c9f060534366e084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.7 KB (641734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9823c5c75857cff14a914de0ec905f26a6c5e708270440fc81b37d866f34bba`

```dockerfile
```

-	Layers:
	-	`sha256:be46a9387b237d188043d207a648edd44f1710856ac276a74dff6913e253597d`  
		Last Modified: Thu, 26 Feb 2026 19:45:19 GMT  
		Size: 597.4 KB (597429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3b2cb2bd8d85be0343f2147231bde9a481651ab6ae44938095046d9a795c67a`  
		Last Modified: Thu, 26 Feb 2026 19:45:19 GMT  
		Size: 44.3 KB (44305 bytes)  
		MIME: application/vnd.in-toto+json
