## `postgres:16-alpine3.23`

```console
$ docker pull postgres@sha256:a5824d29054ed662a86533ab89919d3d7e79987a16e22555f8a98b8a7be45de4
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

### `postgres:16-alpine3.23` - linux; amd64

```console
$ docker pull postgres@sha256:3e42dfb04d4989df191f525d4628c3e4bb56cf71833c44a81dc0e9284693bab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115523176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa391234b15a99d57a67c29db24785f28a33b82af4b7417f581d4a805eedf5c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:50:18 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 19:50:21 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 19:50:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 19:50:21 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 22 Jun 2026 19:50:21 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 19:50:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 19:50:21 GMT
ENV PG_MAJOR=16
# Mon, 22 Jun 2026 19:50:21 GMT
ENV PG_VERSION=16.14
# Mon, 22 Jun 2026 19:50:21 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Mon, 22 Jun 2026 19:50:21 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 19:52:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 19:52:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 19:52:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 19:52:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 22 Jun 2026 19:52:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 22 Jun 2026 19:52:30 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 22 Jun 2026 19:52:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:52:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 19:52:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:52:30 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 19:52:30 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 19:52:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69be66baf45db7b630e9fe27e407261efd5c3482d3ba63ec4191686e6bb88218`  
		Last Modified: Mon, 22 Jun 2026 19:52:46 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a37451f427cb8fa358e00cd2143373e7ab726174dbf09032d3b85a1d3306ba6`  
		Last Modified: Mon, 22 Jun 2026 19:52:46 GMT  
		Size: 900.3 KB (900252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5618177d94acd5e06f344350f32583083a4cea3e582f6d3718c8d37cc47d84cc`  
		Last Modified: Mon, 22 Jun 2026 19:52:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea68d8c51b363af4d77db6a1911f29acba22e787f280ddca74f5461874b4956`  
		Last Modified: Mon, 22 Jun 2026 19:52:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afdc8fd7faa99d8d4edeea38b11002450570fd4e701b46d6cb4b09b58e99d52`  
		Last Modified: Mon, 22 Jun 2026 19:52:51 GMT  
		Size: 110.8 MB (110761052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b8936aa74d7c5eaf604381b186ebe669bc096bf0d321897da16793d1166566`  
		Last Modified: Mon, 22 Jun 2026 19:52:48 GMT  
		Size: 9.6 KB (9617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f36cb436002be6c12ae443b1d24384c9e008130ca620e72f57dd6a0af25011`  
		Last Modified: Mon, 22 Jun 2026 19:52:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff30d81f90c6bd83367444cc05b9fab5de781a2cafc009cf391391c0cb2adf3a`  
		Last Modified: Mon, 22 Jun 2026 19:52:48 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a73fcaeb8bbbd0685a94c2a86453ae6e83ad54c7018f4f0c567bc195d7b700`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decb19dc3c24d91d098ea14a0cd45842b094783ca47f8f87d285fc8cb78278f8`  
		Last Modified: Mon, 22 Jun 2026 19:52:49 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:23cc776c502764ee8cf55477b3a4c79a3fd659559e91bd1203be063499926db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.1 KB (641142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714fe69f566ec078e1d1ca097bf7e12fd473b20679fa67803be2a51bf0e7e029`

```dockerfile
```

-	Layers:
	-	`sha256:89382657ee6398bd0e90586b580575be3334cc59631e43ff1624cbf829d60318`  
		Last Modified: Mon, 22 Jun 2026 19:52:46 GMT  
		Size: 597.5 KB (597458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c06668d3a793fb1b88b1a59789e7698a251fafa085364a60b16124d4660891`  
		Last Modified: Mon, 22 Jun 2026 19:52:46 GMT  
		Size: 43.7 KB (43684 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; arm variant v6

```console
$ docker pull postgres@sha256:396473c56ae5596b3867fb43abbb7d0cf4318c24dfa48c49dc09daa43639d6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111757426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd32b3e013d5120bced567019a038e651f42522ed2cecf46e7d72c57cd2ea4ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:49:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 19:49:50 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 19:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 19:49:50 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 22 Jun 2026 19:49:50 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 19:49:50 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 19:49:50 GMT
ENV PG_MAJOR=16
# Mon, 22 Jun 2026 19:49:50 GMT
ENV PG_VERSION=16.14
# Mon, 22 Jun 2026 19:49:50 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Mon, 22 Jun 2026 19:49:50 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 19:54:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 19:54:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 19:54:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 19:54:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 22 Jun 2026 19:54:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 22 Jun 2026 19:54:41 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 22 Jun 2026 19:54:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:54:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 19:54:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:54:41 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 19:54:41 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 19:54:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf4eea413c7f6bca6f4e387161ea985a2c50a4bc5a3d7346543d5c3fbed752a`  
		Last Modified: Mon, 22 Jun 2026 19:54:53 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ce04ba776e83584bf1352efdb8643e48c4a84904eddc298ec7902f743380d8`  
		Last Modified: Mon, 22 Jun 2026 19:54:53 GMT  
		Size: 864.6 KB (864626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b01318b255aea5297219d82f43cf9e2c8916cdb2d40424cb7e27826a8af236e`  
		Last Modified: Mon, 22 Jun 2026 19:54:53 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4500cfee83ebb06f3fdbda77b1eb7c98a56d909606b5ead385d0652b2633f0`  
		Last Modified: Mon, 22 Jun 2026 19:54:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3409a79e79cdbb7ff2584f36fc04d0dfab454253c55ee448ffd7efa1ea86bb0`  
		Last Modified: Mon, 22 Jun 2026 19:54:58 GMT  
		Size: 107.3 MB (107322759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb0b64244e6b2519c5d0b37a6cbfaa61eba1c155accbd5d0541f728e4a9011f`  
		Last Modified: Mon, 22 Jun 2026 19:54:54 GMT  
		Size: 9.6 KB (9614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee10b72016ed8c361cd82762041768b674fae19b746f7d7c0652ddd734b078d`  
		Last Modified: Mon, 22 Jun 2026 19:54:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb9375c2f9ca7f71f27ef7249e77b4be79efb59d1476a66577d2e02b989275b`  
		Last Modified: Mon, 22 Jun 2026 19:54:55 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80acf7364c5ef76f6244587845f98ad5296e09853ea535a025a3e0754cc3ffa2`  
		Last Modified: Mon, 22 Jun 2026 19:54:56 GMT  
		Size: 6.1 KB (6094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acba4764df9c503ac5bf36c68c580ddf2129eaa93555a9040f42e44cdca03bc5`  
		Last Modified: Mon, 22 Jun 2026 19:54:56 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:9477a19266fe06e076a8141ed4574b5980fcb47382d01a224af4adc39e6a43df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 KB (43637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c8276fb0027be556f87b7b8db8a2382b90dd8b29b7921d64cdbf88dcb69ce7`

```dockerfile
```

-	Layers:
	-	`sha256:cab1855f689acebae7e8cd1a5ef7e55f36c6c23c05c48e70e330b4de368886a6`  
		Last Modified: Mon, 22 Jun 2026 19:54:53 GMT  
		Size: 43.6 KB (43637 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b1586de44a4fcea1a6d11d2e7de8cd0e99a5b0c592d8aaac263c0779693ae933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105465936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec82792276a68104c410d366aa1f06f8993c72409c08d74d4f988b2660121990`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:05:59 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 20:06:01 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 20:06:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 20:06:01 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 22 Jun 2026 20:06:01 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 20:06:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 20:06:02 GMT
ENV PG_MAJOR=16
# Mon, 22 Jun 2026 20:06:02 GMT
ENV PG_VERSION=16.14
# Mon, 22 Jun 2026 20:06:02 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Mon, 22 Jun 2026 20:06:02 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 20:08:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 20:08:49 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 20:08:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 20:08:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 22 Jun 2026 20:08:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 22 Jun 2026 20:08:49 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 22 Jun 2026 20:08:49 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:08:49 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 20:08:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:08:49 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 20:08:49 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 20:08:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec4baffaa04858d36c6813fba24857c79bf707877834a300c928efe90c3951c`  
		Last Modified: Mon, 22 Jun 2026 20:09:02 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8933570fe3fed3c527a283ecb245c5edb84c2cddd0e63a87e904e726f38cc3f4`  
		Last Modified: Mon, 22 Jun 2026 20:09:02 GMT  
		Size: 864.6 KB (864648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edf7a561ff58750ef8d22ecc9a38c7b032fac5af5a0c084c11104dee086efad`  
		Last Modified: Mon, 22 Jun 2026 20:09:02 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f7f167df3c9d25c90eb778942327fc6723a219d2fb801abd67bf530492edb9`  
		Last Modified: Mon, 22 Jun 2026 20:09:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63daf4ae10bd81369bc1b2e1be6610044cb8638227873a32f3c622b7c57be69f`  
		Last Modified: Mon, 22 Jun 2026 20:09:06 GMT  
		Size: 101.3 MB (101321976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c63caf031c3b354c87d533e3dce306730359e299e9aef619d643e05d002356c`  
		Last Modified: Mon, 22 Jun 2026 20:09:04 GMT  
		Size: 9.6 KB (9621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4f79a13f6aafaaee2069a18c4ffb7e9007c7864dcdea4e3cc45d57328c221b`  
		Last Modified: Mon, 22 Jun 2026 20:09:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c4141eba4802f00eb3f8aa50db7fb2110ae9670938cdd1c6b16e0e048eaa94`  
		Last Modified: Mon, 22 Jun 2026 20:09:04 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7850a2c97de87b61163e317d1e7a158ff239266e7bb2246663e920d1302a57e5`  
		Last Modified: Mon, 22 Jun 2026 20:09:05 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43eefa468c265619de28c8d1b7691321017b52520585947b7b2480216890ea36`  
		Last Modified: Mon, 22 Jun 2026 20:09:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:dd20c986a88d4b5be9204730837a652f676ee52034b4372b4257f90d80584a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.7 KB (640680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717f43784363477aa64654a5f1b3a6dbd405f23598a769160a94e71c7ff274d3`

```dockerfile
```

-	Layers:
	-	`sha256:710358227045801cbd0c968b4ae4b8200e50ae2d095f5c88cfa5fdc55d51d712`  
		Last Modified: Mon, 22 Jun 2026 20:09:02 GMT  
		Size: 596.8 KB (596828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:372b922b197107a55820dcc9696861897cf52eca3393e3e2482e44a6c82e5ed8`  
		Last Modified: Mon, 22 Jun 2026 20:09:02 GMT  
		Size: 43.9 KB (43852 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:074c7ef277e1883314ae3b51b2c6c5888e92961dec4b307f643ee5b381d5c515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113343071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d3a735e0f683370164c701a91345c3ea07b12834f42673a49b793663255556`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:51:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 19:51:19 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 19:51:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 19:51:19 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 22 Jun 2026 19:51:19 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 19:51:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 19:51:19 GMT
ENV PG_MAJOR=16
# Mon, 22 Jun 2026 19:51:19 GMT
ENV PG_VERSION=16.14
# Mon, 22 Jun 2026 19:51:19 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Mon, 22 Jun 2026 19:51:19 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 19:53:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 19:53:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 19:53:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 19:53:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 22 Jun 2026 19:53:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 22 Jun 2026 19:53:41 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 22 Jun 2026 19:53:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:53:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 19:53:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:53:41 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 19:53:41 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 19:53:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3932d36115137f858e0ad1f37c24de563be097d29db4051e83a5f40277417c`  
		Last Modified: Mon, 22 Jun 2026 19:53:57 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15a050a74fdb4a61881c6ac3fe904a497d6e3aae9da657edcae906126cb32b5`  
		Last Modified: Mon, 22 Jun 2026 19:53:57 GMT  
		Size: 852.3 KB (852276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca318b2fb02f58955ae70db00cfe7d72ac32ae67fdbbe102e702b1871c3f029`  
		Last Modified: Mon, 22 Jun 2026 19:53:56 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101056f35a1dfc7ab7f577f74f7ff69bbeb6bb14ab75d24a6428994cf472a797`  
		Last Modified: Mon, 22 Jun 2026 19:53:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850edf0c40b233f26b6083beaec4d723db074ed974fa0dbce7786e2d83409252`  
		Last Modified: Mon, 22 Jun 2026 19:54:01 GMT  
		Size: 108.3 MB (108291480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e5f79eba8e60446d6c53f0c145591e796261d353aaa49383a7bae24e4d883a`  
		Last Modified: Mon, 22 Jun 2026 19:53:58 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b8cd4ad07e16a4c7375031e6afe67b3629744a87eb9c2aad4549a7bc5b824d`  
		Last Modified: Mon, 22 Jun 2026 19:53:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392cb0cce0def89374c154c257a9d0bfe7c672630d93ce21b7e79710574493b3`  
		Last Modified: Mon, 22 Jun 2026 19:53:58 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8501090b22cc130a198cafdc0b83c20f2af30f6f438b0f93c0daba091b16d6`  
		Last Modified: Mon, 22 Jun 2026 19:53:59 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f5cbafd84b306c54aa664fd7be1f93438a011b274c490f7ab9ebb0cde144f3`  
		Last Modified: Mon, 22 Jun 2026 19:53:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:4e334cb928ebccaa49d43ecb1bf16207692f31796b23d8093d36e6067243e72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.7 KB (640724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6993b2afe81bd38c6acb3f0232b5862c651cf81c464d8ea54770c964b140139e`

```dockerfile
```

-	Layers:
	-	`sha256:fc7fe9ea28ac598fc8aefe26c8789cb6aa2089ee8fce2e969ddf32006e0a4116`  
		Last Modified: Mon, 22 Jun 2026 19:53:56 GMT  
		Size: 596.8 KB (596840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a41588105705a1e720216c9afd711f03a4db2d4a7e759c5f8e2510256195fcde`  
		Last Modified: Mon, 22 Jun 2026 19:53:56 GMT  
		Size: 43.9 KB (43884 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; 386

```console
$ docker pull postgres@sha256:b9632b9818ad6a45f602f6f2518fbfaeda0e29efebe78d0231a7c0185d24e10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122167707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537844e20ae3ded3e51eaa939e20bf3e0a6a7415e5bc8e93eb36aa120968ac7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:50:18 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 19:50:21 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 19:50:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 19:50:21 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 22 Jun 2026 19:50:21 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 19:50:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 19:50:21 GMT
ENV PG_MAJOR=16
# Mon, 22 Jun 2026 19:50:21 GMT
ENV PG_VERSION=16.14
# Mon, 22 Jun 2026 19:50:21 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Mon, 22 Jun 2026 19:50:21 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 19:53:26 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 19:53:26 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 19:53:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 19:53:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 22 Jun 2026 19:53:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 22 Jun 2026 19:53:26 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 22 Jun 2026 19:53:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:53:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 19:53:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:53:27 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 19:53:27 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 19:53:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0134012f8b50b2f88c3d8f9a8bcefaee91bc1b107ee901d90cef0b27bcface3d`  
		Last Modified: Mon, 22 Jun 2026 19:53:44 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a79de3830d1033655f4ed3aaa5d2f8bab4605e5b80271eefb6c4a5e1f03213`  
		Last Modified: Mon, 22 Jun 2026 19:53:44 GMT  
		Size: 868.4 KB (868448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8618338296e27ba4757ef34f82159a6d53fa2b320b5a264496329468c073413c`  
		Last Modified: Mon, 22 Jun 2026 19:53:43 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea68d8c51b363af4d77db6a1911f29acba22e787f280ddca74f5461874b4956`  
		Last Modified: Mon, 22 Jun 2026 19:52:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b5419fb017a4daebddc6007e2f8c99966a2bca73241a0e160550106c401df2`  
		Last Modified: Mon, 22 Jun 2026 19:53:48 GMT  
		Size: 117.6 MB (117613820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b856b2f269ef36f58ea536e14882053bc16035432748d9105e93c97864f03ad`  
		Last Modified: Mon, 22 Jun 2026 19:53:45 GMT  
		Size: 9.6 KB (9617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97db3e4239570f63c15d8da5e59144a32473101e91848a808205792682d1e559`  
		Last Modified: Mon, 22 Jun 2026 19:53:45 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a8bd1ffde22daba3b12b75bfa96692ef3632b68216482b14d2a72a86e011af`  
		Last Modified: Mon, 22 Jun 2026 19:53:45 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c199b61ccaa31647b3fe3d0584c787edc18fdd40b64ff8c75f189f14731a3f4`  
		Last Modified: Mon, 22 Jun 2026 19:53:46 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da64f9b884dc28e13aa9cbcfe6c8159c3dc6d8c9d221e10d99988bb3cb231ab7`  
		Last Modified: Mon, 22 Jun 2026 19:53:46 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:d04d47d1f749e3c629923c07ca85d912f42a6efd9a62ccaf761d04bf65086477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.1 KB (641088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed04198f1069f888966ca5d9be1a346f70406a5f8d009a6abbb335744eb2fa38`

```dockerfile
```

-	Layers:
	-	`sha256:e16004f223a10b1670c13c68315ba6779a9e5a6bc03b2645152d4565ef40d740`  
		Last Modified: Mon, 22 Jun 2026 19:53:44 GMT  
		Size: 597.4 KB (597443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703325c64f34f698ed1c1ef533677a6e9b4b5ca6ca1df9bc42c4e5e95ce6ef73`  
		Last Modified: Mon, 22 Jun 2026 19:53:44 GMT  
		Size: 43.6 KB (43645 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; ppc64le

```console
$ docker pull postgres@sha256:b8d9987fd7a96349ed67b56a7e9e88ed6d3ab25482d8582521ea33b49ececdaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118207668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4279973d342b31832999efed3a0d28b6c65852dc0bd8aa7a361c310fe5dfd152`
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
ENV PG_MAJOR=16
# Mon, 22 Jun 2026 20:36:04 GMT
ENV PG_VERSION=16.14
# Mon, 22 Jun 2026 20:36:04 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Mon, 22 Jun 2026 20:36:04 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 20:40:04 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 20:40:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 20:40:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 20:40:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 22 Jun 2026 20:40:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 22 Jun 2026 20:40:06 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 22 Jun 2026 20:40:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:40:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 20:40:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:40:06 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 20:40:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 20:40:06 GMT
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
	-	`sha256:ea78e3ee1ba77596ec9945cad1b9bb04cc04e10d189756daf8ab9acda3c10701`  
		Last Modified: Mon, 22 Jun 2026 20:40:46 GMT  
		Size: 113.5 MB (113520425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e6365a304f84841555c3b310d154e475851cdf54682c20b88246b2dcd5ea82`  
		Last Modified: Mon, 22 Jun 2026 20:40:43 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c5ecf5d91f575f89d86fcf0510cf8acd94d6b75c55d02c3f0c75bedbec551f`  
		Last Modified: Mon, 22 Jun 2026 20:40:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a20b3fc6ebb3d980a5c3ff8f12344be39749d112741e5267f946e16815ce3b`  
		Last Modified: Mon, 22 Jun 2026 20:40:44 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3008c55bfa77d0e837e1b8417f05876e49b0e5849692d3528744bbb12f7bcd7b`  
		Last Modified: Mon, 22 Jun 2026 20:40:44 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6630237257144d9f3cf8330cfa442f6ca3a3a3c5ec41ea13801dbd222a1f90a2`  
		Last Modified: Mon, 22 Jun 2026 20:40:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:6aa2635494179e932d493c33378c931cc1c01110dbe8929c36fe0a755661a425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.9 KB (638898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace3b2a8c7dbd9bb282629556c872bec49e0bfa81f45b8f7a1ad4741a47ae08b`

```dockerfile
```

-	Layers:
	-	`sha256:435c6ee310176c3138f06441c40a22c17b3fa8ab1376dbd64f1dd458afd71bd1`  
		Last Modified: Mon, 22 Jun 2026 20:40:43 GMT  
		Size: 595.2 KB (595167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41a6055a389283ae018bbdb4b9b5dc9bb99e645ba437ced1537e3c730bd57250`  
		Last Modified: Mon, 22 Jun 2026 20:40:43 GMT  
		Size: 43.7 KB (43731 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; riscv64

```console
$ docker pull postgres@sha256:8d56e68df5426241db068d6bee574c0df0af9ab325377cc53099b2357acb1944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117614051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda8b8e16c900fadb4e62f87f4365bbe46532d2fd23284f7af76973380c516f4`
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
ENV PG_MAJOR=16
# Tue, 23 Jun 2026 10:03:16 GMT
ENV PG_VERSION=16.14
# Tue, 23 Jun 2026 10:03:16 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Tue, 23 Jun 2026 10:03:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 23 Jun 2026 10:53:38 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 23 Jun 2026 10:53:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 23 Jun 2026 10:53:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 23 Jun 2026 10:53:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 23 Jun 2026 10:53:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 23 Jun 2026 10:53:40 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 23 Jun 2026 10:53:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 23 Jun 2026 10:53:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 23 Jun 2026 10:53:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jun 2026 10:53:40 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jun 2026 10:53:40 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 23 Jun 2026 10:53:40 GMT
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
	-	`sha256:f92d38080c2b6c409a49d2700529a612d8a199cdd276ae559871c3949b53708e`  
		Last Modified: Tue, 23 Jun 2026 10:56:53 GMT  
		Size: 113.2 MB (113178384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39f580f74517da96c6ac4d9b8e224c8aa9d3c91d1d305ff215e71b128feaa04`  
		Last Modified: Tue, 23 Jun 2026 10:56:35 GMT  
		Size: 9.6 KB (9630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340980eb47455d3b240699b6e666d0ed1eefff046ab991aded99a2f5473885a1`  
		Last Modified: Tue, 23 Jun 2026 10:56:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c36111b8f36f29554ecbd7d350d6edeae9dbbb4f37d2fb25fec2fbc34db84d2`  
		Last Modified: Tue, 23 Jun 2026 10:56:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d6dbdb7beb128991ccec14a4041af2f6cab38be2b419449741e114df6f88dd`  
		Last Modified: Tue, 23 Jun 2026 10:56:37 GMT  
		Size: 6.1 KB (6103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df700f8db79df8bd9ef25d434e4e2b366a5e66c207457e00c1f5447d97aacff`  
		Last Modified: Tue, 23 Jun 2026 10:56:38 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:56e60faea242f4628f957b20a8808a91fcb784ad81ddc74940eefabb9862a571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.6 KB (640557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affd8c59ddbed1aa4dffd6a7cb54d4e9173bc2fe93ba3f057d7302c36ce11d8f`

```dockerfile
```

-	Layers:
	-	`sha256:6ef8ab4c222b3f61cdd5a1f139390a6aee213b8a501b3d211285f05d67634dd5`  
		Last Modified: Tue, 23 Jun 2026 10:56:35 GMT  
		Size: 596.8 KB (596825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c29e3cb392622fe3e7f05858bc4d9705c15d5e82c64fa44a0d176856a23498f`  
		Last Modified: Tue, 23 Jun 2026 10:56:35 GMT  
		Size: 43.7 KB (43732 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.23` - linux; s390x

```console
$ docker pull postgres@sha256:bef130d4aeeab9705f43081013b9668756b9ba5583935eda0020d067531eb09a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (122014692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c191765b3cc97ffd83a29136823986faa1d585d8f1d71f5096682bf8342506d5`
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
ENV PG_MAJOR=16
# Mon, 22 Jun 2026 20:03:44 GMT
ENV PG_VERSION=16.14
# Mon, 22 Jun 2026 20:03:44 GMT
ENV PG_SHA256=f6d077142737920858ce958ccdb75c6ee137a63b5b0853c70693d401ac7e3471
# Mon, 22 Jun 2026 20:03:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 20:07:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 20:07:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 20:07:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 20:07:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 22 Jun 2026 20:07:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 22 Jun 2026 20:07:17 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 22 Jun 2026 20:07:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:07:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 20:07:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:07:18 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 20:07:18 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 20:07:18 GMT
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
	-	`sha256:ff60e19d687715bcf0aadaee262ed17788fdf03875b7b5673643759aa6ef8298`  
		Last Modified: Mon, 22 Jun 2026 20:07:46 GMT  
		Size: 117.4 MB (117415487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37036574060b6b2bb9231d76740303b0e81cad19135dd0066d27ffa0c9e024c9`  
		Last Modified: Mon, 22 Jun 2026 20:07:43 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0e81c5f71d885a9d879885d14bf47ae916aff01a5cf1d40d8ec4fd239dae94`  
		Last Modified: Mon, 22 Jun 2026 20:07:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ce4d0de8ff906db72646317d1257ea9be34364e21ef773c0eb8b7217dfa266`  
		Last Modified: Mon, 22 Jun 2026 20:07:44 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97667ca0dfe17b2686699ebf319ec6f9a1f8064ecb263e776eaad0f032574a47`  
		Last Modified: Mon, 22 Jun 2026 20:07:44 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf1804a8666b8396ee1214c46db34c32ee6206aa39cde851c25d7223dee6f5b`  
		Last Modified: Mon, 22 Jun 2026 20:07:45 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:18193282df4b9bf4a23ab2ef7fed7799bc06f24cae69349786be84c2befe7293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.5 KB (640490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7105f8bc6b94c21545247870e9b708ab69744fc0267212549793620e52808b5d`

```dockerfile
```

-	Layers:
	-	`sha256:28afb958918c17f33949f5d824c4a34ea815fafa19e82cd92b1b2bc9661812e7`  
		Last Modified: Mon, 22 Jun 2026 20:07:43 GMT  
		Size: 596.8 KB (596807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42b79a6f3b6a856840fb890afa28d1521a285517826917452b723fd1aeb784cc`  
		Last Modified: Mon, 22 Jun 2026 20:07:42 GMT  
		Size: 43.7 KB (43683 bytes)  
		MIME: application/vnd.in-toto+json
