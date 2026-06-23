## `postgres:15-alpine3.23`

```console
$ docker pull postgres@sha256:713d529a461fc86aa7771a097372bc9abded8ff57d0792274cfda988fbf44245
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

### `postgres:15-alpine3.23` - linux; amd64

```console
$ docker pull postgres@sha256:c91eabd7c76cafd59d8deef5f8721132c2b302cfb9daeb414afa92f76db819c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114700247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f490265ebe3fc561e4eaa1f9a4bd90db6080edec2fdd736ec44a4cff1c5779f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:50:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 19:50:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 19:50:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 19:50:22 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 22 Jun 2026 19:50:22 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 19:50:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 19:50:22 GMT
ENV PG_MAJOR=15
# Mon, 22 Jun 2026 19:50:22 GMT
ENV PG_VERSION=15.18
# Mon, 22 Jun 2026 19:50:22 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Mon, 22 Jun 2026 19:50:22 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 19:52:38 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 19:52:38 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 19:52:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 19:52:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 22 Jun 2026 19:52:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 22 Jun 2026 19:52:38 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 22 Jun 2026 19:52:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:52:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 19:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:52:38 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 19:52:38 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 19:52:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0613b8ac6235244c1863ba3d8e4f9c7b2faaccd8b09c8549deb7a0e8ce21da4`  
		Last Modified: Mon, 22 Jun 2026 19:52:55 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342096ad77323aa34b8595345fffd8872c47b569d542f3aba1797fc229405654`  
		Last Modified: Mon, 22 Jun 2026 19:52:55 GMT  
		Size: 900.3 KB (900252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98bb4dcb3ec39a8aa7d301a1b05891b6efa46f587da419ca7047b775212cc23`  
		Last Modified: Mon, 22 Jun 2026 19:52:55 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf720184efd7f6cc23de4d34dc077d444d9836a1b47262b4c5f01cde8d68369`  
		Last Modified: Mon, 22 Jun 2026 19:52:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4c184c4cb04b730c8f0ddb757d16e418279739fdb39352b7a1a8cb89d01485`  
		Last Modified: Mon, 22 Jun 2026 19:52:59 GMT  
		Size: 109.9 MB (109938290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd51b3a528292c29f04bf0d36ad07e285dc253133de2d26010ddc755832683c6`  
		Last Modified: Mon, 22 Jun 2026 19:52:57 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae63139aaca277b804bbe8b8ca7ecf2da9e0e4e19d0132b1934b74c88c36fd32`  
		Last Modified: Mon, 22 Jun 2026 19:52:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84ecf06560d869f789d928398d77b208f09d39bc4ab2f9d79f6ef5f0b94fa7e`  
		Last Modified: Mon, 22 Jun 2026 19:52:57 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a33587f299640d3cfeba0c1802a3b1f053ba26f8baf75d80205837dbf4ef25`  
		Last Modified: Mon, 22 Jun 2026 19:52:58 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cd1030be44934a34f3a3dc2c4cef0391b3867d2b8a3b5e2f900cc4cc36c0ad`  
		Last Modified: Mon, 22 Jun 2026 19:52:58 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:66543cbb5fc431250806b9348ebaa2cf5d24096526eb3b95688dc8f316f5638b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.2 KB (641226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a95617279ec9b00eb6288e6e3d32b402e32286aa399901e38e26855755eb974`

```dockerfile
```

-	Layers:
	-	`sha256:86ca0aa9064ee49f699fb2196d6b86f0e73df33ffe23499330648c2c5e63e8a9`  
		Last Modified: Mon, 22 Jun 2026 19:52:55 GMT  
		Size: 597.5 KB (597458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:452e1268323a11c1c03a87c1005e2e5151a433b0b36d4bbab08667044908ddf9`  
		Last Modified: Mon, 22 Jun 2026 19:52:55 GMT  
		Size: 43.8 KB (43768 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; arm variant v6

```console
$ docker pull postgres@sha256:8d1200f3d968f330fee582022a758abcc551e44c0552b67772744f4969260eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (111000342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b19b22729b4b4501158b24fcbe63f3ccde4adafbe51a54f0f0fccc57bf00cdf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:49:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 19:49:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 19:49:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 19:49:59 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 22 Jun 2026 19:49:59 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 19:49:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 19:49:59 GMT
ENV PG_MAJOR=15
# Mon, 22 Jun 2026 19:49:59 GMT
ENV PG_VERSION=15.18
# Mon, 22 Jun 2026 19:49:59 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Mon, 22 Jun 2026 19:49:59 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 19:54:34 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 19:54:34 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 19:54:34 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 19:54:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 22 Jun 2026 19:54:34 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 22 Jun 2026 19:54:34 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 22 Jun 2026 19:54:34 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:54:34 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 19:54:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:54:34 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 19:54:34 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 19:54:34 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca145aa5d29c535d45b1b4abe3e4e7c08d225bc0e73fba9edaf0d6803cf7b67e`  
		Last Modified: Mon, 22 Jun 2026 19:54:48 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc36062532ce62f970a8b4ae27e76e929a2762117f1baaa77d64f09e8915b3f`  
		Last Modified: Mon, 22 Jun 2026 19:54:48 GMT  
		Size: 864.6 KB (864629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77cfc5a7e408adab46a0915c2a5664d64ffd2baa61c9f90dc72f460ee516b93`  
		Last Modified: Mon, 22 Jun 2026 19:54:48 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec8d5dd1c627c9d3686b620b6939d1bd89c0dbceda9778046914136fa4a7660`  
		Last Modified: Mon, 22 Jun 2026 19:54:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6f01cbbe3ef3554f8b3c75635c9142783a69390cd7bf58d2f7143bff3f7e0e`  
		Last Modified: Mon, 22 Jun 2026 19:54:52 GMT  
		Size: 106.6 MB (106565830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef0739850f55e99bf53008a09bec418118c4c7a208c421a751ca66d97ac5a39`  
		Last Modified: Mon, 22 Jun 2026 19:54:49 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55117366c931ccbb9ddf6b2399c8df2636ace1999f1de68402282969d2be8350`  
		Last Modified: Mon, 22 Jun 2026 19:54:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c62a1b257edab896f807af636939242cf96fc96bbb06162bdbf8f02b8ba13bf`  
		Last Modified: Mon, 22 Jun 2026 19:54:49 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a396d75bd2040ba94f01f43e21b11ad228e235ed48448a7d1d134ead5acaaf5d`  
		Last Modified: Mon, 22 Jun 2026 19:54:50 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc86f0ca68cd0fa131e40465211b8ac0c97331b94cb71d1ec8e5f7334adb449e`  
		Last Modified: Mon, 22 Jun 2026 19:54:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:334eed9276a980ac5b85e673bdf2997fff50ac11a07d740ac4774c4c6b3d98ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 KB (43721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166c092278a04fe7cdd0ca3a8a54a13cf3ff864141b015bc4181d72c749972f3`

```dockerfile
```

-	Layers:
	-	`sha256:e90c5dc936e7542eed3f643d155da51d7f10a744d4aa580682bf1fce2d287c64`  
		Last Modified: Mon, 22 Jun 2026 19:54:48 GMT  
		Size: 43.7 KB (43721 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; arm variant v7

```console
$ docker pull postgres@sha256:6dd3f8ed5746f61d34003dd43b6b28c0541bc7051f1abf8f2aa20ca7398910fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104734203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ab99861c1f054638b77fc700bd2b65259dddf4dab2638b235b9d110cf083b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:05:50 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 20:05:52 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 20:05:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 20:16:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 22 Jun 2026 20:16:52 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 20:16:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 20:16:52 GMT
ENV PG_MAJOR=15
# Mon, 22 Jun 2026 20:16:52 GMT
ENV PG_VERSION=15.18
# Mon, 22 Jun 2026 20:16:52 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Mon, 22 Jun 2026 20:16:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 20:19:35 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 20:19:35 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 20:19:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 20:19:35 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 22 Jun 2026 20:19:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 22 Jun 2026 20:19:36 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 22 Jun 2026 20:19:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:19:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 20:19:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:19:36 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 20:19:36 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 20:19:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c358234cef465ffd4fa10c77613c464a9bf30683fdab5d4052741f4d0850650`  
		Last Modified: Mon, 22 Jun 2026 20:09:13 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48c0d4fd75f9d80aed5580273a2bbfbc2e95ab66f87d566a7b86853dff83bed`  
		Last Modified: Mon, 22 Jun 2026 20:09:13 GMT  
		Size: 864.6 KB (864638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dbde5f35798db0c10568ffda24407d53480ade98e6305e216fa336bbec7dfcc`  
		Last Modified: Mon, 22 Jun 2026 20:19:48 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4b47ed3692f41fa34af5e5bc94fb028101888fd1eaee24b96a7df7f36ef37`  
		Last Modified: Mon, 22 Jun 2026 20:19:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d65a1b060e1e006998f24d4ed7e82713c2ab0a428ef11a5a8fee820ebe2952`  
		Last Modified: Mon, 22 Jun 2026 20:19:51 GMT  
		Size: 100.6 MB (100590422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1912a30cb4ddea400e7a5fc8380785cfcf0dc1501f7890c89dea6cb8b1f3806f`  
		Last Modified: Mon, 22 Jun 2026 20:19:49 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39fac828b4cb2f6a372f98fabcc04c4938f9bf5b139425fa7fecb5fe9f9ba3f`  
		Last Modified: Mon, 22 Jun 2026 20:19:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fa702493d8c5200f5dc380a81882312321ec0185574700ba5d2fcb5c5d2d42`  
		Last Modified: Mon, 22 Jun 2026 20:19:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec0bfad4ebf17a796e29982d21080ad3e83394c815cdc520db4051419de1b1a`  
		Last Modified: Mon, 22 Jun 2026 20:19:50 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebed382e17e4dcf7168c3ae8ca44328b05d3dd463aa12bb59e25b4acbfe9b139`  
		Last Modified: Mon, 22 Jun 2026 20:19:51 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:ac5355f7d0da8d6fdf5d564502d89d279b3a603ce4eca8551d055c96659263f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.8 KB (640764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d263a3e720708d3cb1d330fb1d9d949a0f2f5caff380caae68e7f42843162fd`

```dockerfile
```

-	Layers:
	-	`sha256:9843dc269e405258ef188cc3ca15dcbf950c6f71086ea8ff25179f0d2034aea0`  
		Last Modified: Mon, 22 Jun 2026 20:19:49 GMT  
		Size: 596.8 KB (596828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7839320486970f2af7646fe150ac9d96d392d9aec164c91eb43322b21006f0ef`  
		Last Modified: Mon, 22 Jun 2026 20:19:49 GMT  
		Size: 43.9 KB (43936 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:3010c5892e8deb852c212758fe280a4ba4436b15ed724e29b589df3560b7e346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112536761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca80b45a04193b8340c8193c62f9f8c03e9c168ace982ceb6bc25ea7fb97e39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:51:59 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 19:52:02 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 19:52:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 19:52:02 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 22 Jun 2026 19:52:02 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 19:52:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 19:52:02 GMT
ENV PG_MAJOR=15
# Mon, 22 Jun 2026 19:52:02 GMT
ENV PG_VERSION=15.18
# Mon, 22 Jun 2026 19:52:02 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Mon, 22 Jun 2026 19:52:02 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 19:54:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 19:54:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 19:54:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 19:54:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 22 Jun 2026 19:54:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 22 Jun 2026 19:54:08 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 22 Jun 2026 19:54:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:54:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 19:54:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:54:08 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 19:54:08 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 19:54:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1a28a7d552935192cc1113691cdc12eb558525725abb999f3beb21f8e0e35b`  
		Last Modified: Mon, 22 Jun 2026 19:54:23 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c4b3158dd350e915065c0300a0d92cfef007ace1dfb89cc71c33d3a8960f98`  
		Last Modified: Mon, 22 Jun 2026 19:54:23 GMT  
		Size: 852.3 KB (852282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ef800de8fad9c3c6bc59f9a6e27ac99952c480567785dafbd75b8e65012c89`  
		Last Modified: Mon, 22 Jun 2026 19:54:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2affa204540c780d5ddf7f94e0987eb56225cda103a37c9c408b71037d528fcc`  
		Last Modified: Mon, 22 Jun 2026 19:54:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797b460740a44373719f2c26d66f98b11bbbb2aee057b0e2c0e2922870f11daf`  
		Last Modified: Mon, 22 Jun 2026 19:54:27 GMT  
		Size: 107.5 MB (107485336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd520591a0fc95cf4d02aa5fd9f614527539b90e57de9c2d2cfcfa1c1fd6ee3`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f043d3347a3b55ef8060b25541daddf9002c0f0fe4e382176c86ba386df0344d`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84111278ebc80accabf1a8d65de6a727e0b7f489567e0c1fa679095bf452d69a`  
		Last Modified: Mon, 22 Jun 2026 19:54:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263be1658c72711fca393293099ac6972c2090a4b25a4bac6714c236acb220f4`  
		Last Modified: Mon, 22 Jun 2026 19:54:26 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca02d7b2eac7b994070a4339794620e31f950c9ed03db72cd3588365a5e1166`  
		Last Modified: Mon, 22 Jun 2026 19:54:26 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:3d958faf8e88404f221c1df8fd3fb8c99524db5c87a692044fcef770c4422fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.8 KB (640806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07bb15c78f0983afcd1ae50948f2355ac50790e671e4be15484e0e891ec77690`

```dockerfile
```

-	Layers:
	-	`sha256:65f26769f114d47c31924a8adc0bbede2db3b6ffbf0a8cdc23a921a7cc796b8e`  
		Last Modified: Mon, 22 Jun 2026 19:54:23 GMT  
		Size: 596.8 KB (596840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3abb42829ebd5d678aa5d7e4cc8ca0044c6cf53c287d0dc2267c1a59ecde09ac`  
		Last Modified: Mon, 22 Jun 2026 19:54:23 GMT  
		Size: 44.0 KB (43966 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; 386

```console
$ docker pull postgres@sha256:3ffef2bbdf978cceaa39d82ed72ec74df06c02834451b810904f0394f9b545e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121389117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15b5d10dfa0c8c0ba3496ab7fbba94680f45881dfdf491d5ce5a727b5346b43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:50:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 19:50:31 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 19:50:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 19:50:31 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 22 Jun 2026 19:50:31 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 19:50:31 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 19:50:31 GMT
ENV PG_MAJOR=15
# Mon, 22 Jun 2026 19:50:31 GMT
ENV PG_VERSION=15.18
# Mon, 22 Jun 2026 19:50:31 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Mon, 22 Jun 2026 19:50:31 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 19:53:19 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 19:53:19 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 19:53:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 19:53:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 22 Jun 2026 19:53:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 22 Jun 2026 19:53:19 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 22 Jun 2026 19:53:19 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:53:19 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 19:53:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:53:19 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 19:53:19 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 19:53:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3f044de511e7001ac08544f6d3b0a20573630a72f242f4839b11bb08dcdc07`  
		Last Modified: Mon, 22 Jun 2026 19:53:35 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b1aa2abccffae2c87dca0086162a65099a4896f46ef90712c06e0fe1c8affd`  
		Last Modified: Mon, 22 Jun 2026 19:53:35 GMT  
		Size: 868.5 KB (868451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d795330db0777ad02e64b11eb2ce32c2b12d6dc690576d2ad4f8def79f34d36`  
		Last Modified: Mon, 22 Jun 2026 19:53:35 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e005245607cc76df08c1b1e5c4c500a2f0ef64bafa741b151ba2bded90a4e1fb`  
		Last Modified: Mon, 22 Jun 2026 19:53:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464a611520c9844ed69b5625f0f2de1fe9a201f8d627a057023df7baf26be218`  
		Last Modified: Mon, 22 Jun 2026 19:53:40 GMT  
		Size: 116.8 MB (116835391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92daf9c2c724f6aa5c3ec67b91a8a82bebbeb56685d044935656da3f56845c0`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915d94dde010ae34a445fc654ba75e512fedb5ac4ba7bd7c9cfec3edb81c51fa`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeee3f38e469012b2ea585a902f66e3ad0bd356758fe0c16ebc8bf37d5680981`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e123ec0cb2f262a2828a4aef38f166621e3fa5388bcf8e5b139002d1f9d9cc`  
		Last Modified: Mon, 22 Jun 2026 19:53:38 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5172428f206147e37030482e696d7dae7be2ae81188661d2e3c653a7b9b200`  
		Last Modified: Mon, 22 Jun 2026 19:53:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:d09f06349761b91bb141c8ffb29607dcda618c3a8711d68181b760c86e0771e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.2 KB (641173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3651017884aa9eecf5883ffafcf883fa3ea443232481ae6761d0bd0bab0c3532`

```dockerfile
```

-	Layers:
	-	`sha256:973b65c3769ceb0da90df1ed84c1f46e44b3d70d61c3d024873a7d6cc5753c42`  
		Last Modified: Mon, 22 Jun 2026 19:53:35 GMT  
		Size: 597.4 KB (597443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0fc75527c0760deeaa8f583c7cfa75f3d718a476a59586aa64dd20d3ebbdf4`  
		Last Modified: Mon, 22 Jun 2026 19:53:35 GMT  
		Size: 43.7 KB (43730 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; ppc64le

```console
$ docker pull postgres@sha256:722944a2fab6fa9aaf3bfdda759b5a8ca14a236470ea02c2ee7f1e0125449f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 MB (117359442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eff7da1126e443d429a59557dcee9d6175b499fd15442a5285876e7efa714b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:30:50 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 20:30:54 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 20:30:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 20:36:03 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 22 Jun 2026 20:36:03 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 20:36:04 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 20:36:04 GMT
ENV PG_MAJOR=15
# Mon, 22 Jun 2026 20:36:04 GMT
ENV PG_VERSION=15.18
# Mon, 22 Jun 2026 20:36:04 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Mon, 22 Jun 2026 20:36:04 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 20:44:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 20:44:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 20:44:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 20:44:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 22 Jun 2026 20:44:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 22 Jun 2026 20:44:42 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 22 Jun 2026 20:44:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:44:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 20:44:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:44:43 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 20:44:43 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 20:44:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e9391c05f944b123f5876a64f7d6915dbe05ee717e4f8f20d4c90a5650ddc2`  
		Last Modified: Mon, 22 Jun 2026 20:35:46 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9021869c82cf45db60d7f76a103a86eaa728469afacae3a8f0f41b2c0cf875ae`  
		Last Modified: Mon, 22 Jun 2026 20:35:47 GMT  
		Size: 857.5 KB (857475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7197d07f2d369aa6f2900c4b4eed0515e5527ffed17d6a2955fac6aae81fe017`  
		Last Modified: Mon, 22 Jun 2026 20:40:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b41cdd0f2c331af50c58bdf059e3ffe1022080601cca1822276a21c682bd22`  
		Last Modified: Mon, 22 Jun 2026 20:40:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9244434cf5cb972b01ef96572385976b05a28cbb8fc6b2303954297c5c6bf1`  
		Last Modified: Mon, 22 Jun 2026 20:45:24 GMT  
		Size: 112.7 MB (112672372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cad8889e59bf4cbe4cffa4ef43f6dbc277c7edc5c2bd395d8c4b42b151655c2`  
		Last Modified: Mon, 22 Jun 2026 20:45:19 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806569eb7b791a57280b09076ca33e8fbe534bcc6b9034f9f2cb649749ea2687`  
		Last Modified: Mon, 22 Jun 2026 20:45:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46af788c7d717de7ffddff61303e70ebce55b4b7bcf3c39a7e94c8beaf83b5e9`  
		Last Modified: Mon, 22 Jun 2026 20:45:19 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbabeff0cc73721a6b109812ba376595a05534228126720d50f7d5a955f09cec`  
		Last Modified: Mon, 22 Jun 2026 20:45:21 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7070689bcb97b773f689d935c593bee0152d263ed0cb9752b0dcc5869d7fd9`  
		Last Modified: Mon, 22 Jun 2026 20:45:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:2b12e211af11a543ea3704af01b4e977d2ad1d657175183b6027b462c78be924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.0 KB (638983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc85418217c833196f88cd375c6aa1f5fb47724c2f44375d60be99a57942bb5`

```dockerfile
```

-	Layers:
	-	`sha256:56dce97fc7ad2547323866443f5459fa089e43989de0271ee6ec0f96b1901810`  
		Last Modified: Mon, 22 Jun 2026 20:45:19 GMT  
		Size: 595.2 KB (595167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5197cd857ce05a2ca60e6cc0b5dfdf5fd94d027acf4d5d73fa7af4d4baa2318e`  
		Last Modified: Mon, 22 Jun 2026 20:45:20 GMT  
		Size: 43.8 KB (43816 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; riscv64

```console
$ docker pull postgres@sha256:b6ee1580dfd4c967210bcf49df15fb6400a92ac51c3c8de0716593c250ab45c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116696207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ca715a8c874d2e60fad50ac420252d5f30d8e003630d6625e045867fbd3164`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:30:17 GMT
ADD alpine-minirootfs-3.23.5-riscv64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:30:17 GMT
CMD ["/bin/sh"]
# Tue, 23 Jun 2026 07:15:11 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 23 Jun 2026 07:15:22 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Jun 2026 07:15:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Jun 2026 10:03:15 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 23 Jun 2026 10:03:15 GMT
ENV LANG=en_US.utf8
# Tue, 23 Jun 2026 10:03:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 23 Jun 2026 10:03:16 GMT
ENV PG_MAJOR=15
# Tue, 23 Jun 2026 10:03:16 GMT
ENV PG_VERSION=15.18
# Tue, 23 Jun 2026 10:03:16 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Tue, 23 Jun 2026 10:03:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 23 Jun 2026 11:46:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 23 Jun 2026 11:46:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 23 Jun 2026 11:46:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 23 Jun 2026 11:46:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 23 Jun 2026 11:46:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 23 Jun 2026 11:46:24 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 23 Jun 2026 11:46:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 23 Jun 2026 11:46:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 23 Jun 2026 11:46:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jun 2026 11:46:24 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jun 2026 11:46:24 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 23 Jun 2026 11:46:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8a1e5860a6401101356d3688f519ef896539fceeb0e505b24a7224fe7e76fdb1`  
		Last Modified: Mon, 22 Jun 2026 19:30:41 GMT  
		Size: 3.6 MB (3573240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cac45ec548c7ccf65b7ccea57c257bf6c8aa845b1f52c0e944db730d107a7f`  
		Last Modified: Tue, 23 Jun 2026 08:10:42 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ca51690a6cbab005a488d9d289f0dffb8791e9037c65b7bb2f724816ea103`  
		Last Modified: Tue, 23 Jun 2026 08:10:42 GMT  
		Size: 844.9 KB (844945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd8df36bc5f23a75817a1f7b76f219cdcb6437a8900fa4766b5375584844dfe`  
		Last Modified: Tue, 23 Jun 2026 10:56:35 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c821a46d9f863a203d39d66c8acc631329a61d26cc6fc1082d82bc9da9feb384`  
		Last Modified: Tue, 23 Jun 2026 10:56:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5a745fedbfd1c18f194840c6207040ec4df8a0f22b42e4366812ad7cb1eaa2`  
		Last Modified: Tue, 23 Jun 2026 11:49:32 GMT  
		Size: 112.3 MB (112260715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc51aac30e48e3fc617329d6454669617244cc8e933ddcb964ee2fa9023c036`  
		Last Modified: Tue, 23 Jun 2026 11:49:16 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6310bced336e628ec7a733fe249a479e54eb926f2dfd889f8575de9187ddd140`  
		Last Modified: Tue, 23 Jun 2026 11:49:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57d93e63f45801204f6b8bdbac64dd2b054b9467e2d3ad6b3c85d53902b19c2`  
		Last Modified: Tue, 23 Jun 2026 11:49:16 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6144e9420a8738678b6559f0afbe0f408a39a7132fdb73b103e66b9d579802`  
		Last Modified: Tue, 23 Jun 2026 11:49:17 GMT  
		Size: 6.1 KB (6103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b19902eb415712076438b870d34e4929be0c5be6c76665dd7f045825f467612`  
		Last Modified: Tue, 23 Jun 2026 11:49:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:69052818d63191038194d3904a6012ad0c10597553171ce10c63b4ef5933a309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.6 KB (640641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23eda9daccc05e25372373437817af74a19992fe2d9a9c87dd7558de6ac09d3`

```dockerfile
```

-	Layers:
	-	`sha256:c47d14a0316931efeb1108b6cbf8fa14e15c675a4c4e8cb4ab3e1e6b7a679a40`  
		Last Modified: Tue, 23 Jun 2026 11:49:16 GMT  
		Size: 596.8 KB (596825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:452b94c7a6cf195067b35777385807bbe01a771ff60616562ad23f0d2ca6362a`  
		Last Modified: Tue, 23 Jun 2026 11:49:16 GMT  
		Size: 43.8 KB (43816 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; s390x

```console
$ docker pull postgres@sha256:385132fb768e66324fab78d73587b7b4ea3db5eda3f0b0cac0cb7b8b0e8336f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121185542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046c5ee092f3239485fd278ccab4d905169eb2b7ca809bf38c51598208dd5045`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:02:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 20:02:17 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 20:02:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 20:03:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 22 Jun 2026 20:03:44 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 20:03:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 20:03:44 GMT
ENV PG_MAJOR=15
# Mon, 22 Jun 2026 20:03:44 GMT
ENV PG_VERSION=15.18
# Mon, 22 Jun 2026 20:03:44 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Mon, 22 Jun 2026 20:03:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 20:09:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 20:09:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 20:09:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 20:09:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 22 Jun 2026 20:09:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 22 Jun 2026 20:09:58 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 22 Jun 2026 20:09:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:09:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 20:09:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:09:58 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 20:09:58 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 20:09:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dcf63c964792512f3f7a826a74a49054cebe7cc1e0ac6e05fa7396806c67cd`  
		Last Modified: Mon, 22 Jun 2026 20:06:19 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfed1bf23e7b1309208c3b686d6f6dc526033533f2b7dbe99ca30e87d28e6bd`  
		Last Modified: Mon, 22 Jun 2026 20:06:19 GMT  
		Size: 874.5 KB (874495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9287e53f8da759e0dfa98edd047315167ee60999bef65456bc9ba270047f15`  
		Last Modified: Mon, 22 Jun 2026 20:07:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c553b990ea69a62c461b341d889c0b6e7076d8d4b67dde16b3f1e90c33b3232d`  
		Last Modified: Mon, 22 Jun 2026 20:07:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d952f8c5803a09c5b1ed1398243858686db4646bdbbe8728bb89eb0823ce7b30`  
		Last Modified: Mon, 22 Jun 2026 20:10:25 GMT  
		Size: 116.6 MB (116586509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac103bf03a09590248333b5ddeec7c6ea3087a0910d9b612a76d81acaea6f12`  
		Last Modified: Mon, 22 Jun 2026 20:10:23 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60df1ba04a536794455c40606bf004eba95a91e13d25e67b850960ffb7816e8`  
		Last Modified: Mon, 22 Jun 2026 20:10:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ae31b31786bdfec797ea61c507a84bd8970cbea5b6046bcfb1f5e2ec03e666`  
		Last Modified: Mon, 22 Jun 2026 20:10:23 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f918b4abc90a95f235a5371611860ce2c3b8ce98764624d622cf3ebec902590e`  
		Last Modified: Mon, 22 Jun 2026 20:10:24 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750dec23284c429dc68f67d8562ba06e6c750b2b17ce96908401ddd92f9455e6`  
		Last Modified: Mon, 22 Jun 2026 20:10:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:891293865beb64d4d10e173cb1376070aaec23ea0c1581bf3d2f0d92a0dfe907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.6 KB (640575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31794d2f26c0987c3017a02bbc9824066b0db4d760a71caf748e4f01793c8584`

```dockerfile
```

-	Layers:
	-	`sha256:8bdd0bd184f6d1242c71e5254963ca89677af463e0ec8183c71482e4902bc269`  
		Last Modified: Mon, 22 Jun 2026 20:10:23 GMT  
		Size: 596.8 KB (596807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:223ea70ee376b046836ab2a0286a3dd81a4c098891f579ac87f7082ed0530b25`  
		Last Modified: Mon, 22 Jun 2026 20:10:23 GMT  
		Size: 43.8 KB (43768 bytes)  
		MIME: application/vnd.in-toto+json
