## `postgres:14-alpine3.23`

```console
$ docker pull postgres@sha256:14f02666642586a64d6fae8ef42d479fd76456a77c73ae8a626b8fe323b76d22
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
$ docker pull postgres@sha256:ecbaf416bee41a51565e5b3ad9c2b5bb9a1cebc62e1ca04047701298f3668bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108532163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1dc23700520f339e7d1902ef81abfa4cf0ee5a7868d925bea31bd6aafe250a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:22 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 00:37:24 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 00:37:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 00:37:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 18 Dec 2025 00:37:24 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 00:37:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 00:37:24 GMT
ENV PG_MAJOR=14
# Thu, 18 Dec 2025 00:37:24 GMT
ENV PG_VERSION=14.20
# Thu, 18 Dec 2025 00:37:24 GMT
ENV PG_SHA256=7527f10f1640761bc280ad97d105d286d0cf72e54d36d78cf68e5e5f752b646b
# Thu, 18 Dec 2025 00:37:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 00:39:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 00:39:31 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 00:39:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 00:39:31 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Dec 2025 00:39:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Dec 2025 00:39:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Dec 2025 00:39:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:39:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 00:39:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:32 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 00:39:32 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 00:39:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e5feb410e895a1fd0e7a9121fe24ffca666de333d3cde8f9d18946014f97df`  
		Last Modified: Thu, 18 Dec 2025 00:39:41 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3048a283a43359eaef3a7a922cb39eb67377b94a7a35f45ac6bab59b3b724a89`  
		Last Modified: Thu, 18 Dec 2025 00:39:55 GMT  
		Size: 922.9 KB (922932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fbe13bb5767f6d3a636c2dab5d678afe006c121a3298b7317c11893ff377e4`  
		Last Modified: Thu, 18 Dec 2025 00:39:42 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060e3656c1863a1bed9ae6859f79ab413babdc4d7574d406979e40258bcb1380`  
		Last Modified: Thu, 18 Dec 2025 00:39:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ddc8f8bcd280ddf8bd598a0197fc30f13320e73de2fa7b4e026a4b023c7d26`  
		Last Modified: Thu, 18 Dec 2025 00:39:50 GMT  
		Size: 103.7 MB (103732340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2773b0333db942b5a83fffde5aa77631e67df15d59b0a0bde6c53a9e51e907`  
		Last Modified: Thu, 18 Dec 2025 00:39:48 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c8de051a19464145696ec83cc25cbcc94fc95671b65c87a31db9ad710a7d5f`  
		Last Modified: Thu, 18 Dec 2025 00:39:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a94049536b3b990e620c71d6fb2316477dbaea64ebb49c58d5273656d1d441`  
		Last Modified: Thu, 18 Dec 2025 00:39:49 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d06b54013727bf0aef698b65895ea39e2419b1d090f94969a14e59e28fda9a`  
		Last Modified: Thu, 18 Dec 2025 00:39:55 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a48150017a21d2f6b268b358408e3dd672961ad56a730b6750549bd2157b281`  
		Last Modified: Thu, 18 Dec 2025 00:39:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:46665e26cbf917d5818c728b72e3848e13e66dc4c32811db2bb477c6f63c3106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.2 KB (642151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0942fd0a02b3dbcbd9585d6ca22438322354d000023712ab48c71b978e0855`

```dockerfile
```

-	Layers:
	-	`sha256:b1b77887d114471bddaa59629b0a0a088ccdaa7fc13c6b0031e472c2c4ff3996`  
		Last Modified: Thu, 18 Dec 2025 00:39:48 GMT  
		Size: 598.1 KB (598080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b41f3d7510b5b7383cd4f22c3f64a8f843fd53763f48b9465c1be01125b067b7`  
		Last Modified: Thu, 18 Dec 2025 03:07:48 GMT  
		Size: 44.1 KB (44071 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.23` - linux; arm variant v6

```console
$ docker pull postgres@sha256:b267a8288a1a7bfee3e5f2b7374e3193edd47db0985daceec837cb315e2aab75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88035818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d08c594ab857b9c8e14197e56f6e3b10f447f3f1a7d6b4ff02288aaa34057e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:47:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 00:47:51 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 00:47:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 00:47:51 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 18 Dec 2025 00:47:51 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 00:47:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 00:47:51 GMT
ENV PG_MAJOR=14
# Thu, 18 Dec 2025 00:47:51 GMT
ENV PG_VERSION=14.20
# Thu, 18 Dec 2025 00:47:51 GMT
ENV PG_SHA256=7527f10f1640761bc280ad97d105d286d0cf72e54d36d78cf68e5e5f752b646b
# Thu, 18 Dec 2025 00:47:51 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 00:50:35 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 00:50:35 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 00:50:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 00:50:35 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Dec 2025 00:50:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Dec 2025 00:50:35 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Dec 2025 00:50:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:50:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 00:50:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:50:35 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 00:50:35 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 00:50:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9529f1800892a66a3838b34dd730cf9628cec992e58b89f4883fa9fe05049365`  
		Last Modified: Thu, 18 Dec 2025 00:50:46 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f35702f4fe8a3ecaebe44f71f9f2b73dc7998be86fa9c79d0ab28c51d40d72`  
		Last Modified: Thu, 18 Dec 2025 00:50:46 GMT  
		Size: 889.5 KB (889472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d340396292c53ea1960395d1610ef824d307b92cb0f20e22e197ca393507740c`  
		Last Modified: Thu, 18 Dec 2025 00:50:54 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d53ffd7b27ae140d485b51515f43beff5f03e0a08677ef461bd22a1dacdb41`  
		Last Modified: Thu, 18 Dec 2025 00:50:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45365f4a572619b3966eafc33c4e24d925701943bfff7670cf510275c8255b69`  
		Last Modified: Thu, 18 Dec 2025 00:51:05 GMT  
		Size: 83.6 MB (83561142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51176eae769e57a3e17f090a9fd893830a97f0f255498891e4a2ac38ff0be6a9`  
		Last Modified: Thu, 18 Dec 2025 00:50:54 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8eb411ff286b674a942e9b3c63f359db717f420d1cacdac4c73f8bd9656498`  
		Last Modified: Thu, 18 Dec 2025 00:50:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5495f34dedfab2b4969dc4db19236f1e913c48b8d091f82c15d5ed1115c99641`  
		Last Modified: Thu, 18 Dec 2025 00:50:47 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14563ac80a3bddde16303f2728efe1d9de84102e2e0142a69d01124e01bea53f`  
		Last Modified: Thu, 18 Dec 2025 00:50:54 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1df5ac4cc15eb478d30ff9f25ced9b8e2e0aed3a2df9636bc5916c1f0e9f2de`  
		Last Modified: Thu, 18 Dec 2025 00:50:48 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:e8750f5411fd2704e5c81ae854e1e87092155fbbdb026ae42721309c46178969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 KB (44034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8c0ed78113e9fb5f9a97b7d63c6ec51f9e63233ef0b3ed2984a530db6d7624`

```dockerfile
```

-	Layers:
	-	`sha256:8a2af82d26e64b823d7a13443aa1ac95c0df0fd0bfdbc00ccce1eb73eb6636b6`  
		Last Modified: Thu, 18 Dec 2025 00:50:46 GMT  
		Size: 44.0 KB (44034 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.23` - linux; arm variant v7

```console
$ docker pull postgres@sha256:e3bdc169bbc679d9af810fe86cad1d66d25af4c76276304a8e582c4a7b65f695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83294200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80ce189e363a746be3368940550ae2c7ec960a64a5a844d92ba683611a94194`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:45:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 00:45:27 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 00:45:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 00:48:32 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 18 Dec 2025 00:48:32 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 00:48:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 00:48:32 GMT
ENV PG_MAJOR=14
# Thu, 18 Dec 2025 00:48:32 GMT
ENV PG_VERSION=14.20
# Thu, 18 Dec 2025 00:48:32 GMT
ENV PG_SHA256=7527f10f1640761bc280ad97d105d286d0cf72e54d36d78cf68e5e5f752b646b
# Thu, 18 Dec 2025 00:48:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 00:51:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 00:51:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 00:51:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 00:51:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Dec 2025 00:51:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Dec 2025 00:51:06 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Dec 2025 00:51:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:51:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 00:51:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:51:07 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 00:51:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 00:51:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c54560c889f4335681276f8006934bf52e4b177d237ff206c5dd5983c093f`  
		Last Modified: Thu, 18 Dec 2025 00:48:29 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9357d8fc3629d45c7e5e204823a20084bc2d55d8be9f123aacbde58e2854e15e`  
		Last Modified: Thu, 18 Dec 2025 00:48:29 GMT  
		Size: 889.5 KB (889513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c761a7100b0d1cfd1add55578534ca0734023ab7cd86632af0ea431dae0d2bf7`  
		Last Modified: Thu, 18 Dec 2025 00:51:33 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a08d7eb8b6790548f23d7fc5cb053a54074fc555fffc848883957a802a8dca3`  
		Last Modified: Thu, 18 Dec 2025 00:51:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce3e6c2b20b50c161bf23b0dceb662b34baaeca0a51ecb178771c09591dd5cd`  
		Last Modified: Thu, 18 Dec 2025 00:51:34 GMT  
		Size: 79.1 MB (79108520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf763138580bdc39d95244cf26fcb6598d81c8acbe76f1575ba304e07671d4f`  
		Last Modified: Thu, 18 Dec 2025 00:51:28 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8146cbd46e3fcc07c3af8aefc1bf24719f5f5b7c2e841fe8f1b9f71057d74cc`  
		Last Modified: Thu, 18 Dec 2025 00:51:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5d40a0fc73c10f91a24a59a38d6b34ae24b327eb16c6ab4533829a12df6e3e`  
		Last Modified: Thu, 18 Dec 2025 00:51:29 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966df2c590e3b9d28cf0e33bb5bba58b034bacbe7372989e1524ccd02a385c23`  
		Last Modified: Thu, 18 Dec 2025 00:51:20 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9744bcfdcb302eb7cdd7ddd9fba43502456669c998e2c70ac97d816cc9a0df64`  
		Last Modified: Thu, 18 Dec 2025 00:51:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:fef064957e6ecdad75e1bfe551339209760b7c7ea107dba23270cc8385b4d129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.7 KB (641715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd1eb687e293181ce23f9d831dced70e6d0177bfd84ffd97c647e27a49d673a`

```dockerfile
```

-	Layers:
	-	`sha256:7d8ea045435f6800aa8f79449208013fb92a1ae681e00255b299d972b72ab3dc`  
		Last Modified: Thu, 18 Dec 2025 00:51:18 GMT  
		Size: 597.5 KB (597466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:994199c777e185b395f69815687c76ec6094cc2dcb090746cd295090f041c458`  
		Last Modified: Thu, 18 Dec 2025 03:07:55 GMT  
		Size: 44.2 KB (44249 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:aaeb9bdb3cad3cde087949dd130760908f7815fd52e9b755492c68779063a86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106734563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca42e1b812a41cbdf57115b0cf43717a26cb3d3c7200cac05e420cd8d08459fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:11 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 00:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 00:39:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
ENV PG_MAJOR=14
# Thu, 18 Dec 2025 00:39:14 GMT
ENV PG_VERSION=14.20
# Thu, 18 Dec 2025 00:39:14 GMT
ENV PG_SHA256=7527f10f1640761bc280ad97d105d286d0cf72e54d36d78cf68e5e5f752b646b
# Thu, 18 Dec 2025 00:39:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 00:41:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 00:41:22 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 00:41:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 00:41:22 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Dec 2025 00:41:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Dec 2025 00:41:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Dec 2025 00:41:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:41:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 00:41:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:41:23 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 00:41:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 00:41:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb50751834512cef358f57a374ce0c922456bf8bdf24cbc0ca35760b4906cfd6`  
		Last Modified: Thu, 18 Dec 2025 00:41:37 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e14e46911ca345cd43aa3662de4de703d8281af8740aebeb4c59e4ad5959e2`  
		Last Modified: Thu, 18 Dec 2025 00:41:47 GMT  
		Size: 876.5 KB (876478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255695018e33d4ad1b4960ab40b1c2a90da9cf7dd02fb648125b362823c2a973`  
		Last Modified: Thu, 18 Dec 2025 00:41:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b771a89c0b315f69c25893b1b5d85275d037e207b70465a2ab1a027bdc548c`  
		Last Modified: Thu, 18 Dec 2025 00:41:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acfc5f7cb57ff2333533513341c40bcfbed789a6037bcef303ae6afc143ee49`  
		Last Modified: Thu, 18 Dec 2025 00:42:02 GMT  
		Size: 101.6 MB (101645568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b94c3b621c85c4722b721ccc68c984e9c8d278d00d8f398cbe7c84c97031f0`  
		Last Modified: Thu, 18 Dec 2025 00:41:47 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246c86e63ce080762272108d75ad141c7aa1962e722b6061845a4ecff4d60e7e`  
		Last Modified: Thu, 18 Dec 2025 00:41:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab50c2dbe0f3bc098586274856ea4c9f799c6ebe838e298a3b4428abf64f5fb`  
		Last Modified: Thu, 18 Dec 2025 00:41:39 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b277a86d7da8cb84f96be646f83cdfa42c4c98142f0af69c3006961361365ab`  
		Last Modified: Thu, 18 Dec 2025 00:41:47 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5b6dc2f2cd5ec6ec88191e7af550ab486de8a20ffa67a78bc2f369ed2e7b6a`  
		Last Modified: Thu, 18 Dec 2025 00:41:40 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:58c2c107508046945ed1eea5e03f51bf72290677b2754f6d51dfda21bd5e8eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.8 KB (641780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3577ec115858f0d9d04fa93169b06035ab7f672055cdc9269ed6c3c3cab1e0`

```dockerfile
```

-	Layers:
	-	`sha256:b98ad261d980d034d83f935f5052542409e8cdd9d5b1822f0aaacb6a1f22b0c3`  
		Last Modified: Thu, 18 Dec 2025 00:41:38 GMT  
		Size: 597.5 KB (597486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb3b7fab371b399d615cda094ed748a696a038d935c44815667e894449fa3ac4`  
		Last Modified: Thu, 18 Dec 2025 00:41:38 GMT  
		Size: 44.3 KB (44294 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.23` - linux; 386

```console
$ docker pull postgres@sha256:df852d122662b3a4ef0662daf3572ec3f6251924fbd2e44bc5d9d8ed252ae767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114550830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bf595b1f43924b627f2dd169e2a926fe8730fa8e91f91a86a6574fec119cde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:38:21 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 00:38:24 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 00:38:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 00:38:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 18 Dec 2025 00:38:24 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 00:38:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 00:38:24 GMT
ENV PG_MAJOR=14
# Thu, 18 Dec 2025 00:38:24 GMT
ENV PG_VERSION=14.20
# Thu, 18 Dec 2025 00:38:24 GMT
ENV PG_SHA256=7527f10f1640761bc280ad97d105d286d0cf72e54d36d78cf68e5e5f752b646b
# Thu, 18 Dec 2025 00:38:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 00:40:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 00:40:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 00:40:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 00:40:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Dec 2025 00:40:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Dec 2025 00:40:33 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Dec 2025 00:40:33 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:40:33 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 00:40:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:40:33 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 00:40:33 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 00:40:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402a51106aa2596373ab5bc188d15f251cc74a9f7e0e6136b387a0e180f821bc`  
		Last Modified: Thu, 18 Dec 2025 00:40:57 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00751aaf2090445ec214e925aa4a6372704b149cf081ab64914716e09f93a320`  
		Last Modified: Thu, 18 Dec 2025 00:40:48 GMT  
		Size: 893.2 KB (893249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8671ad6c1e4ac6d51e4ba7c34db08b305504bf556fec68e1aa792326b5a2eba`  
		Last Modified: Thu, 18 Dec 2025 00:40:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ccab469b1e286b5e3e479cf051db53870dbdefefa536732a2ac06047fe6e5e`  
		Last Modified: Thu, 18 Dec 2025 00:40:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54dd5497c2ca0e8e5ff091def47fce8112d5e77d165ac1f185e9bacfeff4b34e`  
		Last Modified: Thu, 18 Dec 2025 00:41:07 GMT  
		Size: 110.0 MB (109954703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d444aa8d52db227182537b0ae8dc3143ef9e9c7b7accbe7cb0e22098c8485315`  
		Last Modified: Thu, 18 Dec 2025 00:40:49 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e1f2ee50257272828bbcf9e731b65c9fce298a1d0c557be629a98859939e68`  
		Last Modified: Thu, 18 Dec 2025 00:40:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0cc01d8f950011a7868049de41a8fdaf52d69ec9258fce2d8149172ddb38f5`  
		Last Modified: Thu, 18 Dec 2025 00:40:49 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee23d1d1322d12140dc919f8e136de73c3ca81f027eab7ba62ce4bae5c46dc91`  
		Last Modified: Thu, 18 Dec 2025 00:40:50 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab6c4cdd5c1bced5932ad546159afc886133744d95156b6f99bfbdcc544b9f4`  
		Last Modified: Thu, 18 Dec 2025 00:40:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:ac0ff68e59dafe548b9fb7f96b4a379857f79ac0158efe2042204964a5dbf7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.1 KB (642078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f074cdac4937094e62e8a34b08847e087afb9329dc94c89ed441aa98360665bb`

```dockerfile
```

-	Layers:
	-	`sha256:73b8a4cdfac9e38e8106f777c3e9f92f382e2e2f8906a9a0ccb461d081fa38b5`  
		Last Modified: Thu, 18 Dec 2025 00:40:48 GMT  
		Size: 598.1 KB (598055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:271a046ad05520dca0161f469d0f7f203cde91589fb0b50b854325a2dfe0ea39`  
		Last Modified: Thu, 18 Dec 2025 00:40:48 GMT  
		Size: 44.0 KB (44023 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.23` - linux; ppc64le

```console
$ docker pull postgres@sha256:a799778fd57534e17230bb973d5d7df88e40eaeb96983e8e78a153b62eefd278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93365777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e7c159b15b963337eb022dbad2f2e48b2ce37db9422882cdd23071e6b0a309`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:23:31 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 01:23:37 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 01:23:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 01:27:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 18 Dec 2025 01:27:15 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 01:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 01:27:15 GMT
ENV PG_MAJOR=14
# Thu, 18 Dec 2025 01:27:15 GMT
ENV PG_VERSION=14.20
# Thu, 18 Dec 2025 01:27:15 GMT
ENV PG_SHA256=7527f10f1640761bc280ad97d105d286d0cf72e54d36d78cf68e5e5f752b646b
# Thu, 18 Dec 2025 01:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 01:34:42 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 01:34:42 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 01:34:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 01:34:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Dec 2025 01:34:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Dec 2025 01:34:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Dec 2025 01:34:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:34:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 01:34:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:34:44 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 01:34:44 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 01:34:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:42 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff80bfb816c7f5a841f48ccc8340de9f38d3ad53202d1114a5d309378c7e4c`  
		Last Modified: Thu, 18 Dec 2025 01:26:51 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a7bf1ce9f177344350a6b5de388d3492ef2eee83822d55eb5653a1e893a773`  
		Last Modified: Thu, 18 Dec 2025 01:27:00 GMT  
		Size: 881.5 KB (881524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef3774e02f66275039ec450631fe6e5b7c5de5ade853d0353cd9ea07ada7cf2`  
		Last Modified: Thu, 18 Dec 2025 01:31:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164435015427598747f1483897002e9036fe27b49b12766e70cb1efcdbff8e45`  
		Last Modified: Thu, 18 Dec 2025 01:31:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c9387aba48f09bdf9351dbf8574be23385180f27e92b58ca2c8d178be5eba4`  
		Last Modified: Thu, 18 Dec 2025 01:35:31 GMT  
		Size: 88.6 MB (88639706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1be27273ddebe499e7747fdae4b92888fbaa7480ec92a2adcfdcad63f9fe5d`  
		Last Modified: Thu, 18 Dec 2025 01:35:25 GMT  
		Size: 9.2 KB (9209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72518eca748ac6991a334a035d9a35719141eb5d0258cad4ac2b7e39492e178`  
		Last Modified: Thu, 18 Dec 2025 01:35:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dbefb0bc64360a4ce6709aab9e1d60ba87bd2d3dfe875029b407e230c42ebf`  
		Last Modified: Thu, 18 Dec 2025 01:35:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5668362e757df9e6493b08ed84dc2e0b4b67a0eeda7af3e30185bc04124f8430`  
		Last Modified: Thu, 18 Dec 2025 01:35:15 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a0cd5e5eed1d376fadf193fa8c03b666654744573f92a7a3ebbbbcc907abca`  
		Last Modified: Thu, 18 Dec 2025 01:35:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:61f5514c6dedda8caff24e7bbeede4c87b1bb07093799adfb1f2da002c4df86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.9 KB (639926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d716cd255f2d44aed5435e8fa68d8a415f69969aa27c885b0287b075e3a65da`

```dockerfile
```

-	Layers:
	-	`sha256:3561d93d48e7ed4265d254f3b155873f22349b191b42c7618f74773720d370bc`  
		Last Modified: Thu, 18 Dec 2025 01:35:13 GMT  
		Size: 595.8 KB (595801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d83226d506b24a6f7303caddb41fff4e7643034dd2dbf165a1e852d759eae23`  
		Last Modified: Thu, 18 Dec 2025 01:35:13 GMT  
		Size: 44.1 KB (44125 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.23` - linux; riscv64

```console
$ docker pull postgres@sha256:1145d1705e2185a1728c2db0b6b5dd670135a5a8a6f069fe1e1f56e54bf4a56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109458815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457330eb869348b0ee55fb7859740d25dff3137053056e48e2519454f3ceaeb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 22:58:49 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 22:59:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 22:59:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 19 Dec 2025 00:50:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 19 Dec 2025 00:50:52 GMT
ENV LANG=en_US.utf8
# Fri, 19 Dec 2025 00:50:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 19 Dec 2025 00:50:52 GMT
ENV PG_MAJOR=14
# Fri, 19 Dec 2025 00:50:52 GMT
ENV PG_VERSION=14.20
# Fri, 19 Dec 2025 00:50:52 GMT
ENV PG_SHA256=7527f10f1640761bc280ad97d105d286d0cf72e54d36d78cf68e5e5f752b646b
# Fri, 19 Dec 2025 00:50:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 19 Dec 2025 05:32:33 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 19 Dec 2025 05:32:34 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 19 Dec 2025 05:32:34 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 19 Dec 2025 05:32:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 19 Dec 2025 05:32:34 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 19 Dec 2025 05:32:34 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 19 Dec 2025 05:32:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 05:32:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 19 Dec 2025 05:32:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 05:32:35 GMT
STOPSIGNAL SIGINT
# Fri, 19 Dec 2025 05:32:35 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 19 Dec 2025 05:32:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e7504fb8b5ca902553810400e8ecf856a5984c36fb7dba7b9d1932f5432750`  
		Last Modified: Thu, 18 Dec 2025 23:52:05 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254154902548782aac7bbe74d12c713d81df39d8b697e905a7ada02053473207`  
		Last Modified: Thu, 18 Dec 2025 23:52:05 GMT  
		Size: 868.9 KB (868948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7363523f3adbe06817ea37caa9e4e6b3624d1fb0dbdee981cef69302f9c9c01`  
		Last Modified: Fri, 19 Dec 2025 04:43:55 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d460fd12a197206addf50ae676cb3647196c9d8d1bd09a30c6dcc460442fc4e`  
		Last Modified: Fri, 19 Dec 2025 04:43:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d856c3dc87b2683d9f0b80c5d50dddb7b7a77b6e7f62b33e108546586c73a08c`  
		Last Modified: Fri, 19 Dec 2025 05:35:37 GMT  
		Size: 105.0 MB (104989129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178555681c5350aa3ca31a14fcd48572fd5d9e71e8c457b878911355c44bbbc4`  
		Last Modified: Fri, 19 Dec 2025 05:35:46 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d6f08d08b10b84992458d255a92d08266932d72e3a87d916e7c49b983b9110`  
		Last Modified: Fri, 19 Dec 2025 05:35:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2794abac9c156ca6ff27a88de3edfb7b4ba2434de87c25894299bdf54d9af420`  
		Last Modified: Fri, 19 Dec 2025 05:35:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39dc497dcf1d2efae5749ff5466b76d711f7a22094eb3c141f0b68f62af9fc4f`  
		Last Modified: Fri, 19 Dec 2025 05:35:46 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66af693a52ce31bc4df715bb8e4f345b2bd0df95c6c45487f3cc36cb1aaf54ed`  
		Last Modified: Fri, 19 Dec 2025 05:35:46 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:38e98d38514221c1f402eced42818113e402f4a2192bf8371a92947f4c4af678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 KB (641589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5aa4c59d13d8c07107dd1ba294433fff070f7a57793336a6bea2558b9c7d87`

```dockerfile
```

-	Layers:
	-	`sha256:b2cdf34735cbfd7543418fc09eb368dedba10b6c24bb19f32f957c42de68ea68`  
		Last Modified: Fri, 19 Dec 2025 09:07:33 GMT  
		Size: 597.5 KB (597459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fd5fc1681246989cd60e819cfc9c927b2965cf9471d10dbf05aca8282fd1952`  
		Last Modified: Fri, 19 Dec 2025 05:35:21 GMT  
		Size: 44.1 KB (44130 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.23` - linux; s390x

```console
$ docker pull postgres@sha256:2c9b906ff994f57ec5ada261d6486be8cb4d7308645b9a628b47698c783fbb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116648434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993e106557a3523542b27d6fd720678442a58d176b498671a59ea1f5872477fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:06:33 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 01:06:36 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 01:06:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 01:07:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 18 Dec 2025 01:07:52 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 01:07:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 01:07:52 GMT
ENV PG_MAJOR=14
# Thu, 18 Dec 2025 01:07:52 GMT
ENV PG_VERSION=14.20
# Thu, 18 Dec 2025 01:07:52 GMT
ENV PG_SHA256=7527f10f1640761bc280ad97d105d286d0cf72e54d36d78cf68e5e5f752b646b
# Thu, 18 Dec 2025 01:07:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 01:17:04 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 01:17:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 01:17:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 01:17:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Dec 2025 01:17:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Dec 2025 01:17:06 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Dec 2025 01:17:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:17:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 01:17:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:17:07 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 01:17:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 01:17:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47640600947e6c2716121eaeecb21eafc3f56109bbf28a6b3637e7e493750c2`  
		Last Modified: Thu, 18 Dec 2025 01:11:27 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72711bc192b3b7fee821ed917f13059104e610eeefe93d04d8ae5148c6065ce3`  
		Last Modified: Thu, 18 Dec 2025 01:11:40 GMT  
		Size: 897.4 KB (897412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf4323059ef6bbfafcfdcbf1d2a523cfa88a34caa32895a4eddc6bf00c26db7`  
		Last Modified: Thu, 18 Dec 2025 01:12:46 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6436d9eb64b8c72abf73201c7930932dea7566031c1c8eab90d757110587f026`  
		Last Modified: Thu, 18 Dec 2025 01:12:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221fe159e454d130871f6dbfeba19758b277aae19060ee97843fecb039b58e1f`  
		Last Modified: Thu, 18 Dec 2025 01:17:51 GMT  
		Size: 112.0 MB (112009923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef5bcd796a0ae51b080c3b6088638cbcc1bac1e163db1f39db79105086120ea`  
		Last Modified: Thu, 18 Dec 2025 01:17:56 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf9a4521aa356433d2f5b50318f526c4cc34c0b5b6851faca1c99d55d7a4a97`  
		Last Modified: Thu, 18 Dec 2025 01:17:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc16b57da516893412b84a212f503f6597de7b4fd1c28ea4041562f1788c2b9`  
		Last Modified: Thu, 18 Dec 2025 01:17:56 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab966f93675670b35468533d5343bc8bbf42a36e24fdbf38302bddcfcbf22dda`  
		Last Modified: Thu, 18 Dec 2025 01:17:48 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688d0c952b48e399db7e93da5d1247a95665aa5ef7db211a521eef77b880a503`  
		Last Modified: Thu, 18 Dec 2025 01:17:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:bc518271277585dddca5c32721a5664c4999cc61e42d865151766338e33d03cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.5 KB (641500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5947e48cbed55b941b44960d4e1d8b72dcc1f561884d4cf7601552f8915ccc13`

```dockerfile
```

-	Layers:
	-	`sha256:81aa50d226c3b5d48635b6040e5c1f7b3044d1a9839df2b8bdf1ae6f50193a8f`  
		Last Modified: Thu, 18 Dec 2025 03:08:25 GMT  
		Size: 597.4 KB (597429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbc3b04f769a811ed287a99485e6101e0a11e4b98ddf7e99423145808f39ef89`  
		Last Modified: Thu, 18 Dec 2025 03:08:26 GMT  
		Size: 44.1 KB (44071 bytes)  
		MIME: application/vnd.in-toto+json
