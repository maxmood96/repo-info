## `postgres:16-alpine3.19`

```console
$ docker pull postgres@sha256:1abbdd8c5bfb10ba18bb39a447e0a6980754f51e2dafb5541988743fb0a01144
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

### `postgres:16-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:e163085cfece956f7f384675c5a712f7833f808953fae4c1af0fef4ea882f1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96838218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbca26429e8e4870a8b7848c5c0be61a60e85bc2c9e2796cbcb7763819a2b7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=16
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=16.3
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119249d35d967146460adfe87946533c3a781fd3b679f139342f6336da035392`  
		Last Modified: Mon, 22 Jul 2024 23:10:18 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67722bbfe021c6f147d93d7e8d704a1248f2778f22a4779b4650dfd7e21cbc2`  
		Last Modified: Mon, 22 Jul 2024 23:10:18 GMT  
		Size: 1.1 MB (1120290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e249951f0041f5b5011d957682649e460f32879a99dd34afd70766392c77039c`  
		Last Modified: Mon, 22 Jul 2024 23:10:18 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b6bdbaed0f3b64a703c978a27982b46bbf1956743a6aba52702ff3322e867`  
		Last Modified: Mon, 22 Jul 2024 23:10:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba55ec6120c31320853d81931354fe8174f4fd6171c7203707167fd82fcf3d2`  
		Last Modified: Mon, 22 Jul 2024 23:10:22 GMT  
		Size: 92.3 MB (92281876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b1f5611a8a8d926eb1673e981203a00a1526b3961cb07e5cc6521945190789`  
		Last Modified: Mon, 22 Jul 2024 23:10:19 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9897301441fe66bc9b406a0c217f7799fa91755562a0255d9d0a86149ec4225d`  
		Last Modified: Mon, 22 Jul 2024 23:10:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9122945ca1d538d57a3bc020b41b29d34c52bb30dcdca855463cb046239a0d5a`  
		Last Modified: Mon, 22 Jul 2024 23:10:19 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee634af3733eafd7ec0763f1ed5f1b270dae79cd463a66dc57e8c3a6c9b0843`  
		Last Modified: Mon, 22 Jul 2024 23:10:20 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48223395880293ab82d07ee857745839a97ee8a6d8f3e30728857de3ae308f1e`  
		Last Modified: Mon, 22 Jul 2024 23:10:20 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:5de73392e140cd39bc503a551e33d0721a66ce5005c260eb1c8a5fec5499d595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722dcd941d6bab25d61a474fdb99ce8fbb833009f643161f2670dfc00bd4544a`

```dockerfile
```

-	Layers:
	-	`sha256:c6780f0270581f26ea33ccee41d8950620837d2d9a7bc6bcf22c7a6210b34f8c`  
		Last Modified: Mon, 22 Jul 2024 23:10:18 GMT  
		Size: 969.0 KB (968991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b466a3c1841f6a1130926b3a0bac8e804f16001621bd7709e04cc37f12cfd1cc`  
		Last Modified: Mon, 22 Jul 2024 23:10:18 GMT  
		Size: 45.1 KB (45137 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:4f36c70d92b8db8c2748e442a186fa0ccb5c846ed761bb7dd20f923c3464af95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95522544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6162f93e86f5400029db084a9e6b8f241e37bbd49487275e76e0ced70790c8ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=16
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=16.3
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92db845726b4ef5f8ebe5ba287fd7c32243caf3658933582eec2af1b0f3a7a50`  
		Last Modified: Tue, 23 Jul 2024 07:35:04 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc40a1c8b107e2354a2c6161d4558c68f9ccb273de07130617b20be1864e0e7`  
		Last Modified: Tue, 23 Jul 2024 07:35:04 GMT  
		Size: 1.1 MB (1086685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7a7c27725775b797fbb65df1c7553975bc14ee097a441de7576c2534ee4e4c`  
		Last Modified: Tue, 23 Jul 2024 07:44:12 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c5332f31a71b5fc187466578a120e93a96b9922d5d3d6d60d1ace3b4ed05a8`  
		Last Modified: Tue, 23 Jul 2024 07:44:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c7976be60022632b0698386f575caa64af3b90cebbe1feb63ff81bb5d2da74`  
		Last Modified: Tue, 23 Jul 2024 07:44:15 GMT  
		Size: 91.2 MB (91243169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8122049cd602f50f84a7bf2af5be5c76a3796e872feffd25103cca44bede5f`  
		Last Modified: Tue, 23 Jul 2024 07:44:13 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b738ef0883ebf34a931ce5a0c1aade4ca8cc4e112f10171fba3fb2154f7fc0`  
		Last Modified: Tue, 23 Jul 2024 07:44:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c99c0f7f27275e99cb0fed84fe4de09a8fc3f5fd763686880c0f2acfee3f3e2`  
		Last Modified: Tue, 23 Jul 2024 07:44:13 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95028fab762fc515891a9657cb2bb4ac005c4adebcc472f30b39dbd75c484037`  
		Last Modified: Tue, 23 Jul 2024 07:44:14 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87b989ee64aeadb57707798f76e9b343b361eecd514548a021afff7fab947f0`  
		Last Modified: Tue, 23 Jul 2024 07:44:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:127ec5fbac5559e7a2d0eb824ff9807e175c023599e79fdb8e1040ca06c48169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 KB (45083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a438ea70d798cba18cc33db4d631b9f20f5de0b4b7d07b8be6b466e6bb00e55c`

```dockerfile
```

-	Layers:
	-	`sha256:3086b5cd8f5c74cec9bda913f72bf5757669772101a9a093941e157bb4bc8bfc`  
		Last Modified: Tue, 23 Jul 2024 07:44:12 GMT  
		Size: 45.1 KB (45083 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:6e1f1d01676bd5735a986e93022a16d090776653bec9973586b6b7c261193ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89968681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ecd5c5eedb87c2c7dd8d466cc6486622de614b53c92c1f25924de7e549dbf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=16
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=16.3
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e00ac6be43720c25c11d5f9f235cecbdb349b24568030205dbbc1527d0a2090`  
		Last Modified: Wed, 24 Jul 2024 03:47:29 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707689daf83e36f961b1d519207e7b06605e5f2b6c48bf51fb093eafc652af18`  
		Last Modified: Wed, 24 Jul 2024 03:47:29 GMT  
		Size: 1.1 MB (1086690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82c88f55a4ec532d4721d7d78cbd5bc8ccb32eec36ee04bae8f80546d6a2e9b`  
		Last Modified: Wed, 24 Jul 2024 04:23:57 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09cfc889019313c567344f8b705116887f023214f894333c8ab5d8049c3ce68`  
		Last Modified: Wed, 24 Jul 2024 04:23:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa483acd4d34169b034da72a3ee60a9a3f392ac7d7c71736c52f83fc18cb75ab`  
		Last Modified: Wed, 24 Jul 2024 04:24:02 GMT  
		Size: 85.9 MB (85937876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b843e383ed8e893e70426b9057008b7d01b0a04d77eda0e915166fa039264eb`  
		Last Modified: Wed, 24 Jul 2024 04:23:58 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11cd33d68c10fbf7e8699efaa584e77593f3008f559998156ca576ca29f4082a`  
		Last Modified: Wed, 24 Jul 2024 04:23:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bb37ea67ed28d34ce96ef6b48b58b481d767f683eba90bec93ba020f40ddab`  
		Last Modified: Wed, 24 Jul 2024 04:23:58 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e24558685f34ed1ad87207c070e0547a66c535e3f14b147d5ae598074298b0a`  
		Last Modified: Wed, 24 Jul 2024 04:23:59 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727881d23168c477e9e7d4eadc424ae9abfb04940ba5988113ccc1302277ea38`  
		Last Modified: Wed, 24 Jul 2024 04:23:59 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:67e4545e9d4d768cec537c22080b52daff09d21843ee83bb46f180bc19fdc814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f5e551ca0488f9bebc9a6137204fff3ef41c24cab5e0a93ed89f0693a7acfe`

```dockerfile
```

-	Layers:
	-	`sha256:dec5e4532aef1a158d01779617d1cae280cf2207f40a738b97bbe17a9324572a`  
		Last Modified: Wed, 24 Jul 2024 04:23:58 GMT  
		Size: 969.0 KB (969019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63b6f813904467fb3db1c345216f5ee9a24abf7a6a7dedb336e852e7e96087e3`  
		Last Modified: Wed, 24 Jul 2024 04:23:57 GMT  
		Size: 45.3 KB (45303 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:78f007c45f9829836cc26c7a02bf418f7744f6a330286376315d262d90fe2b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95525325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca009ed393f4e3293570106fbaa8fa3fc123557fe558c217b84147426708a6d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=16
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=16.3
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7430eedfdfd07b02b245d76061e40a66e9d046eb109fb1dadf11e64547b096`  
		Last Modified: Wed, 24 Jul 2024 01:24:14 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991d9a143b679519e244cf5746ea3f0804454479728e9c8b07bdeb57b3b0e6f3`  
		Last Modified: Wed, 24 Jul 2024 01:24:15 GMT  
		Size: 1.0 MB (1049350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf93a3cb67aebfa1677daa91e5038804bd389b6299c087d01c6f76a9839cdce`  
		Last Modified: Wed, 24 Jul 2024 01:32:37 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446cd68e49014f9aff26d9af569920030ce9d9c3309f9f9bfa9dd0380254bea1`  
		Last Modified: Wed, 24 Jul 2024 01:32:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7f9c54e4adf482664a612cde1ce7769d896395a53428ac801e92b9d4e13e9d`  
		Last Modified: Wed, 24 Jul 2024 01:32:40 GMT  
		Size: 91.1 MB (91100505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e191a54a6728d8b404a05cae96b4ee085b1782cf24e637c7d3db9508a2322a`  
		Last Modified: Wed, 24 Jul 2024 01:32:38 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc7669b82099875106b3097145a72fcfa5366c71304ef6c7d02bc681a2a32e4`  
		Last Modified: Wed, 24 Jul 2024 01:32:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42415fc6006efd0046f9122262604b7bedb26c17468b839ffbfe1af9ef4d4c75`  
		Last Modified: Wed, 24 Jul 2024 01:32:38 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927361941862f09507bc2425715b833a9e1b25efd974af771f5fd88a85ec8ba8`  
		Last Modified: Wed, 24 Jul 2024 01:32:39 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6eadcabbbe5cb9d460f572e766cedc2ca4aa531b29a61951986bb4b621b1d90`  
		Last Modified: Wed, 24 Jul 2024 01:32:39 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:148aca90ade927a045a5d3c8dcc2469fac35153ee83ab7e68de65800d91d15dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6025ea8bfb8a3d7d9f1e321ef191018000e86cf3e33aa89984b8a51eb5ca35`

```dockerfile
```

-	Layers:
	-	`sha256:5a63c7c538c35864c22b5920adfbd4b7314daee25ed0d20211cc9346342deecd`  
		Last Modified: Wed, 24 Jul 2024 01:32:38 GMT  
		Size: 969.0 KB (969035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e65305229fc99642fce56a7effce5c77cfdf2b1a3f107cfb4a4dfd24ed4e77`  
		Last Modified: Wed, 24 Jul 2024 01:32:38 GMT  
		Size: 45.4 KB (45424 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:a89a5452fd6c705db41ba8f3782cb442917ee8c39b76cd745598b2e9ccc8d655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102089325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a21d80fb1e88914221d84b5d471751a8860f5a8a0b0db509199738a4b650f11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=16
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=16.3
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6b177c85f842aa414f71b92cde1a1fcc8fe14d0bdc84914e23721c7a0b4027`  
		Last Modified: Mon, 22 Jul 2024 22:15:24 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114ea4c369ad086f7d3732a6b18a27677a6c8aa47cd0c08555a910132518ea34`  
		Last Modified: Mon, 22 Jul 2024 22:15:24 GMT  
		Size: 1.1 MB (1095470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcad3fadbe020a7e93bebc5914f45239e881f2dd9dff4924d727598153261dfd`  
		Last Modified: Mon, 22 Jul 2024 22:15:24 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e52abd7df90e4bda1bec270bbf89cf95572b37703f9f8d78d1f67d29687aa2`  
		Last Modified: Mon, 22 Jul 2024 22:15:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1039d37df7853bbaf4c7eb95514f8a2d71aad1d8e505248e37e3c02eac120ae3`  
		Last Modified: Mon, 22 Jul 2024 22:15:27 GMT  
		Size: 97.7 MB (97724251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05774883be3c668f4d65d72945089c5be34038a65843ebcabfc1734dc18e6858`  
		Last Modified: Mon, 22 Jul 2024 22:15:25 GMT  
		Size: 9.6 KB (9558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dd7905a6669101a46576a379a3b2a79db5bc8424b6371467f6a35362a6d847`  
		Last Modified: Mon, 22 Jul 2024 22:15:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fe5569bb7990abfee34e65392b92c3a5b6894e76030e55be0031c9bebe1912`  
		Last Modified: Mon, 22 Jul 2024 22:15:25 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3747bd377cc2b1c54548cd1d2bfcc11dd8ebc9055cb0c545f75367d39d7021e`  
		Last Modified: Mon, 22 Jul 2024 22:15:26 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3ea52a1a00a4dfcccdaec574373aeb5d18e7c655bd9149c7889d106e38b18e`  
		Last Modified: Mon, 22 Jul 2024 22:15:26 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:3803241e3880f00b1cbd7835ad4f9a558678bc5faf9983eb357bc873f6ca294b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1014068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fd85fb8aa05d023cc15ef885bf6c067a8e069db95f69e6b91be2a5ca6f5db0`

```dockerfile
```

-	Layers:
	-	`sha256:527d3ac636d587df7d1e6d76a00dc964c0d6e5aabafc7b8eb9e93f58fdf0614a`  
		Last Modified: Mon, 22 Jul 2024 22:15:24 GMT  
		Size: 969.0 KB (968971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7211fe08f6ff3bc6cfb49435cd6e8daf8ac273df07328c3d7fb902841d7e297f`  
		Last Modified: Mon, 22 Jul 2024 22:15:24 GMT  
		Size: 45.1 KB (45097 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:86c6ab42cd1c188f6c40e5f606526dd2254f0fa15df5661d57f2670ac0265f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101395089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e68e4473577498628d4f0fa9bd3a4b3e8a5e524465ae40472aa4ed9cc5a92f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=16
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=16.3
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330cbbf50ded2e8625229e0d1e3964baec3bd1e5d5ed44264ab099a2b5e848ad`  
		Last Modified: Tue, 23 Jul 2024 23:23:42 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff859a6049bfe7ca7de74b2eba16642ac6dc3d517e4a0e82b8a945e876f9a19`  
		Last Modified: Tue, 23 Jul 2024 23:23:43 GMT  
		Size: 1.0 MB (1039694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4fe8ac10c74e56495df6b59aa5abeabfde6a5e29f97d4f59665314537dbbab`  
		Last Modified: Tue, 23 Jul 2024 23:33:17 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae769bd801e43c04b8598e0cf5b7075888000ea67abea2d20bc80c69eaa5ad85`  
		Last Modified: Tue, 23 Jul 2024 23:33:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a6e44f54cb469191eb15620ba40626794ca5ace1a8088eb25dc15482120a94`  
		Last Modified: Tue, 23 Jul 2024 23:33:21 GMT  
		Size: 97.0 MB (96975271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6504befecaae71639f7941201d9a2ed3b7618b6348742e6414eef7e528316dfb`  
		Last Modified: Tue, 23 Jul 2024 23:33:18 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6232ba003cb368253e7d68807f0ad11c150dfe4d27008f989011cbdd34a7e3d`  
		Last Modified: Tue, 23 Jul 2024 23:33:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e976dae13136ff22e3c36ec38f8fa6d45b1626eb3895ae09f2c7ae515472d6`  
		Last Modified: Tue, 23 Jul 2024 23:33:18 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f97dc491b1a8c0c22e9b44de51de499bfc1e5ce4001cf8a03ada08da377ae4`  
		Last Modified: Tue, 23 Jul 2024 23:33:19 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738e79121d5866ccf66a99200d1621f6a85d30375641dbe15829081cf92ae95b`  
		Last Modified: Tue, 23 Jul 2024 23:33:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:1031fa620518a5cc46de7b386666ae70b8009a0922a9eda3cc94c1a7479a80ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b951b29db69c748425b003bb6fccda2e00def7bc0418509e1b12532e1a626c`

```dockerfile
```

-	Layers:
	-	`sha256:e20dbfc703ddf4d93dcb0e12ad226a8f2647e25bb048ec5751389e762e714ef1`  
		Last Modified: Tue, 23 Jul 2024 23:33:18 GMT  
		Size: 965.4 KB (965401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1512fe8c6b081f73d6fb2c37bfbd3020d4916933cd059fb1e9e409d88d2de4f`  
		Last Modified: Tue, 23 Jul 2024 23:33:17 GMT  
		Size: 45.2 KB (45185 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:1e4978766837bef1595aeb77696ef4635507e3f4d277ca825f8931db91dd3205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105718046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3915c440bf7037bb6d25b24d8154d969fbd38a4fde8143d8b668a6af152e4c51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=16
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=16.3
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a29d9d18637c0fb6d9c43edc04cb197f68cc8695789c1b8783e7ec487ee7e1`  
		Last Modified: Wed, 24 Jul 2024 02:29:35 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad71b789841929b348e9494efffad7d755d93cd961944ae2e8763f697e162c9`  
		Last Modified: Wed, 24 Jul 2024 02:29:35 GMT  
		Size: 1.1 MB (1083899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff303435aa88cdece9b5dd2faa434d46a63cda4d2e116304df6de125bdf1a95`  
		Last Modified: Wed, 24 Jul 2024 02:41:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05718277fc1b9b61c11a10cfa85b56974ab1ec3c28091bf8f3eb779c3f94af1b`  
		Last Modified: Wed, 24 Jul 2024 02:41:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de6c17d39f1b3862ba75f1f1c591589431487e91a908a2d55840cb8311bc858`  
		Last Modified: Wed, 24 Jul 2024 02:41:21 GMT  
		Size: 101.4 MB (101364044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985202f50d5b3f15ea24b8d6eee6fa119cf61a116df12fa70458631f3c64f9fe`  
		Last Modified: Wed, 24 Jul 2024 02:41:19 GMT  
		Size: 9.6 KB (9567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0c06b502cc9d9e8ad918e8df7c8a51fcb38164c642e75c36e0d47b80950b8f`  
		Last Modified: Wed, 24 Jul 2024 02:41:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272b223d73324adc77328f80b3713a8a5a8ba12577118977d2ffa3489b6ab5fa`  
		Last Modified: Wed, 24 Jul 2024 02:41:20 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a65bb8ba758f2b25850fbc770c3d44387450d20329a7ef719542af7ee938f03`  
		Last Modified: Wed, 24 Jul 2024 02:41:20 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216f06637b4ba3b33097007bfb6c8ec92dcf86687f4cfba011c86d42c7bfd7f1`  
		Last Modified: Wed, 24 Jul 2024 02:41:20 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:a254aac2df9c033dc229895fb3f30a2fb9d8f54252ed21cefabec36feb376fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1012179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca48ecafc3d4268ac548d60433c0e4bd72359a801c679eaee3480978c85f9036`

```dockerfile
```

-	Layers:
	-	`sha256:f5655055b7aa19b99ba2af679c2052f76efdf06d06fa301314d74e47c585781b`  
		Last Modified: Wed, 24 Jul 2024 02:41:19 GMT  
		Size: 967.0 KB (967037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b38f6434b2c03a60acda0805a023605cedb78509a7640f836bc5fd38b674e5b7`  
		Last Modified: Wed, 24 Jul 2024 02:41:19 GMT  
		Size: 45.1 KB (45142 bytes)  
		MIME: application/vnd.in-toto+json
