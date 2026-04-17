## `postgres:16-alpine3.22`

```console
$ docker pull postgres@sha256:b285bf2574651c4aebc6eeb7d1223bd56fffe4159b832d1e200efb26c2f2c321
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
$ docker pull postgres@sha256:245a4d1e4fed6704e75cf5709c878ccd849021154b39084a7bb5724f83522141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109530968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7735a8aa38e211b6b46746556c1bd3312676710de580e3a0494579db8a9711e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 17 Apr 2026 00:19:08 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Apr 2026 00:19:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 00:19:08 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 17 Apr 2026 00:19:08 GMT
ENV LANG=en_US.utf8
# Fri, 17 Apr 2026 00:19:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 00:19:08 GMT
ENV PG_MAJOR=16
# Fri, 17 Apr 2026 00:19:08 GMT
ENV PG_VERSION=16.13
# Fri, 17 Apr 2026 00:19:08 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Fri, 17 Apr 2026 00:19:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 17 Apr 2026 00:21:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 17 Apr 2026 00:21:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 17 Apr 2026 00:21:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 17 Apr 2026 00:21:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 17 Apr 2026 00:21:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 17 Apr 2026 00:21:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 17 Apr 2026 00:21:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:21:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 17 Apr 2026 00:21:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:21:30 GMT
STOPSIGNAL SIGINT
# Fri, 17 Apr 2026 00:21:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 17 Apr 2026 00:21:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9d229bff673cb907553178e1006a3d87ce0472762f32f17d17afec6002daf`  
		Last Modified: Fri, 17 Apr 2026 00:21:46 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4e98e45b7afb1560a0f1add2bd178daf5e4f3bfd04ca6ef3476068598f622c`  
		Last Modified: Fri, 17 Apr 2026 00:21:46 GMT  
		Size: 917.4 KB (917425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a12dae442373d3323543ea1470a9c7d1359fafe4bda42cb79ba0053b1740a0`  
		Last Modified: Fri, 17 Apr 2026 00:21:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782505a4a9ce79b083c07c89de44538bed03ff1628d9b60b6d5c05083bd658ad`  
		Last Modified: Fri, 17 Apr 2026 00:21:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e0fb965d6f1e07fb070b76a053deebffb0bacbb152db3ac7e0e44dcf5d60de`  
		Last Modified: Fri, 17 Apr 2026 00:21:50 GMT  
		Size: 104.8 MB (104788149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51762b08e08dfd48278dcb9aa6247ccfdb65f78e4f11e5d83d7b4ccefe7871c`  
		Last Modified: Fri, 17 Apr 2026 00:21:47 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1c2aac4014b433512f925230301d3bd106129f2f4f1b585931547272ffd35f`  
		Last Modified: Fri, 17 Apr 2026 00:21:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f879a33c1460ff4a7185732ae509db2d0b7293ba2d00d40953379f7992bb99a`  
		Last Modified: Fri, 17 Apr 2026 00:21:48 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52695cc9ab16369d44aedc03540281dae08ed6ff906c09b1ca326ae428ecc03`  
		Last Modified: Fri, 17 Apr 2026 00:21:49 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4992da1c7819e72f3a15e9e6d93262655b38461f3a8ce19a2fd51542cf52390`  
		Last Modified: Fri, 17 Apr 2026 00:21:49 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:68f7dd8647368e2d40d7bffbfe8d49fa0f8f45e642395e945d4947ed9f96f116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (639999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e03785c0e3d22ee095a0eb0467c4e421b1f572bc5a0936f2cf1c6432065b89`

```dockerfile
```

-	Layers:
	-	`sha256:1456e894ced229753256d57e6a1ca0f982b0b27190ce880ef8625c4c10376ada`  
		Last Modified: Fri, 17 Apr 2026 00:21:46 GMT  
		Size: 596.3 KB (596315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1214aab55127a67a67dce216acf4141b716c6ee132f8fe70403bbc1a5473c68`  
		Last Modified: Fri, 17 Apr 2026 00:21:46 GMT  
		Size: 43.7 KB (43684 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:bc0bd855ba909bb94024b23100f4fee70d009625d3a68064ff4a768c26593ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89063501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8073eaea4b251fb0170c9682b0937e9e66a0549d9e762dda20bac38b9369b2b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:22:58 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 17 Apr 2026 00:23:01 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Apr 2026 00:23:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 00:23:02 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 17 Apr 2026 00:23:02 GMT
ENV LANG=en_US.utf8
# Fri, 17 Apr 2026 00:23:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 00:23:02 GMT
ENV PG_MAJOR=16
# Fri, 17 Apr 2026 00:23:02 GMT
ENV PG_VERSION=16.13
# Fri, 17 Apr 2026 00:23:02 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Fri, 17 Apr 2026 00:23:02 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 17 Apr 2026 00:25:51 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 17 Apr 2026 00:25:51 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 17 Apr 2026 00:25:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 17 Apr 2026 00:25:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 17 Apr 2026 00:25:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 17 Apr 2026 00:25:51 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 17 Apr 2026 00:25:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:25:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 17 Apr 2026 00:25:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:25:51 GMT
STOPSIGNAL SIGINT
# Fri, 17 Apr 2026 00:25:51 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 17 Apr 2026 00:25:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fbcddfc14768081b22ac3b09761b2ebc9191ec36bcdef42550504f33e140ce`  
		Last Modified: Fri, 17 Apr 2026 00:26:01 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd5765a476bff951571c3b12e234d8c487219c582ce9b8174e1fa7bfdad58f8`  
		Last Modified: Fri, 17 Apr 2026 00:26:01 GMT  
		Size: 885.1 KB (885144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c408d0b2ee82055f2e7537f2485d3ac47b666a73a907593256bea147cfe85fce`  
		Last Modified: Fri, 17 Apr 2026 00:26:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a272cad67f1beaf4b6c36c7d39ae1c70968ff13d517af1f21721b311035e15c8`  
		Last Modified: Fri, 17 Apr 2026 00:26:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54880a5ede79cbfc72f364efbe00d5420d0000142cb1931b3418f4b32d5488bf`  
		Last Modified: Fri, 17 Apr 2026 00:26:05 GMT  
		Size: 84.7 MB (84653775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7dfca7b154130a11a36b303f05bc96be099d8db70881b7bc78f183b721868`  
		Last Modified: Fri, 17 Apr 2026 00:26:02 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47813fe6c0ab27b11a1c1c813db31c479c70c8061ccb26678a30cb55b65ebae3`  
		Last Modified: Fri, 17 Apr 2026 00:26:02 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47db3ebc5633cead082b4727619ef4ecae2c35e793141ecf298599af1ee004a`  
		Last Modified: Fri, 17 Apr 2026 00:26:03 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43164d669e9d1421df0850df614f1f6f7e2aed65f54507de0e8749a5c5ad69a3`  
		Last Modified: Fri, 17 Apr 2026 00:26:04 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1e16ab02552f393b75454a7496d10595127c43d84ad8118f05c5f2f3a5a5e1`  
		Last Modified: Fri, 17 Apr 2026 00:26:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:93c8951c64a9d6f5a2df60721d77c8a62424578d25393804990790adf2513e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 KB (43631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57cc1589f1f989508f39f14413fac32ff297db32a584b01816912e7796bd810f`

```dockerfile
```

-	Layers:
	-	`sha256:42e872e2d1477eb7a740be3e742481cdedccc536d6308a806bed6480a86a46f4`  
		Last Modified: Fri, 17 Apr 2026 00:26:01 GMT  
		Size: 43.6 KB (43631 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:0223bbd89880c55016d5875007d1ffe557d8326afa9b4850eb07dae92e5df33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84342869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ad922a518ccc96525fc33d5f77a1b9eac34183a38e133ed3912b0a6a82f480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:25:10 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 17 Apr 2026 00:25:13 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Apr 2026 00:25:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 00:25:13 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 17 Apr 2026 00:25:13 GMT
ENV LANG=en_US.utf8
# Fri, 17 Apr 2026 00:25:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 00:25:13 GMT
ENV PG_MAJOR=16
# Fri, 17 Apr 2026 00:25:13 GMT
ENV PG_VERSION=16.13
# Fri, 17 Apr 2026 00:25:13 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Fri, 17 Apr 2026 00:25:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 17 Apr 2026 00:27:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 17 Apr 2026 00:27:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 17 Apr 2026 00:27:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 17 Apr 2026 00:27:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 17 Apr 2026 00:27:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 17 Apr 2026 00:27:59 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 17 Apr 2026 00:27:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:27:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 17 Apr 2026 00:27:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:27:59 GMT
STOPSIGNAL SIGINT
# Fri, 17 Apr 2026 00:27:59 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 17 Apr 2026 00:27:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe93795cada09b77b0eb68eb9b8623f855f2d1c4341a60a410ed6fcbeb60dd5`  
		Last Modified: Fri, 17 Apr 2026 00:28:11 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c618c70f53d8567d8d969b86117fa615b96cf6515b3f18f5939de06fd7d4413`  
		Last Modified: Fri, 17 Apr 2026 00:28:11 GMT  
		Size: 885.2 KB (885151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd3e23a2c5412378c5d12b9a3c617db02da194610bcdfe623e17fcf834bba22`  
		Last Modified: Fri, 17 Apr 2026 00:28:11 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6517abb6fdc51c8a25068e58bf7e7a6eb45c21b6284156962f6c189ef955cce8`  
		Last Modified: Fri, 17 Apr 2026 00:28:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3523d1b627457d246dc7154262bfc837fcc3ce0a5ba8bf2153ca7acdc002ef`  
		Last Modified: Fri, 17 Apr 2026 00:28:14 GMT  
		Size: 80.2 MB (80214690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecb36c9a4ed291b67f7b2424350d58bb7359b17431956a101190b10eec014b2`  
		Last Modified: Fri, 17 Apr 2026 00:28:12 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a4af5f9b3fed2b4b1d763e1da2b9e97e111f288cccda0c712008d0aa740bba`  
		Last Modified: Fri, 17 Apr 2026 00:28:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a656f7b4dee2ae2d872479182d6648155c2e9db3ebd87955bfae0d8fba0e455b`  
		Last Modified: Fri, 17 Apr 2026 00:28:12 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc1aedfad7a684d1522c9b034da0a66b592ef142f05e69a40815e1e8f36fbf5`  
		Last Modified: Fri, 17 Apr 2026 00:28:13 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c431d7b0516fefe152fa85c4ff29f57f10e28579081a3bbb7cd8a2d64a4cbc`  
		Last Modified: Fri, 17 Apr 2026 00:28:13 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:32fa571f4d688c2772f0efe6ed802f241ccaf6d14aefcbddca79e988ae420ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74242f68849a977fac5f34dc3a37d0153060a2f746a71c4fa3ba512f3e31e5a4`

```dockerfile
```

-	Layers:
	-	`sha256:eb53309a160dca208df2fa3892e1e3f5803c8891924044ec52b9988db807b7da`  
		Last Modified: Fri, 17 Apr 2026 00:28:11 GMT  
		Size: 596.3 KB (596335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca4d7db2f1e27b29348fcca682bc93c4f8da2c566dbd864c2d0d0a7a70ab398`  
		Last Modified: Fri, 17 Apr 2026 00:28:11 GMT  
		Size: 43.8 KB (43845 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:7e3cb827475f072c883a8b37dd0a6ee1a408f8dce17c7592acc55e55d8ced192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105474712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b11efb0ad89f01933a5c4bcd6dc4cb9bb48d487c699de9baff45319194ecaf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:59 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 17 Apr 2026 00:20:03 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Apr 2026 00:20:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 00:20:03 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 17 Apr 2026 00:20:03 GMT
ENV LANG=en_US.utf8
# Fri, 17 Apr 2026 00:20:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 00:20:03 GMT
ENV PG_MAJOR=16
# Fri, 17 Apr 2026 00:20:03 GMT
ENV PG_VERSION=16.13
# Fri, 17 Apr 2026 00:20:03 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Fri, 17 Apr 2026 00:20:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 17 Apr 2026 00:22:33 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 17 Apr 2026 00:22:34 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 17 Apr 2026 00:22:34 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 17 Apr 2026 00:22:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 17 Apr 2026 00:22:34 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 17 Apr 2026 00:22:34 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 17 Apr 2026 00:22:34 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:22:34 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 17 Apr 2026 00:22:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:22:34 GMT
STOPSIGNAL SIGINT
# Fri, 17 Apr 2026 00:22:34 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 17 Apr 2026 00:22:34 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89f57bf5b82b099b1e254a1eafd0eda527809a25ddd694274c08a0289b83431`  
		Last Modified: Fri, 17 Apr 2026 00:22:48 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df13b5066ce78a3c649577df92dbc65e5512bd6a1f804889e8e5ded1839e9a4`  
		Last Modified: Fri, 17 Apr 2026 00:22:48 GMT  
		Size: 873.1 KB (873131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3518d5f74862c967a1b4bb440451e09f2fcf7c60e1bf3fd864ef033a82203`  
		Last Modified: Fri, 17 Apr 2026 00:22:48 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcddbfa7d9d09fb5c9c81d9b5bd8f94af1a7d11f98466a65e703ea7e138d2dc`  
		Last Modified: Fri, 17 Apr 2026 00:22:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b778b2479d83d98a2a6a58bbe1c6458cfac511b16fe3dff693c0e2f280895c5`  
		Last Modified: Fri, 17 Apr 2026 00:22:51 GMT  
		Size: 100.4 MB (100442482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bad82d667883757320f7effcc82f9860be083196c66e33694fb97f4af2940b`  
		Last Modified: Fri, 17 Apr 2026 00:22:49 GMT  
		Size: 9.6 KB (9621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43a21e8ddb3ad2d6cacc63d5e0cfae322b14266418caf1eba771f4825a15b85`  
		Last Modified: Fri, 17 Apr 2026 00:22:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7b201920db057f51cb88750ccaef85a70f610f45dd835c3823c37bd2a4dd6f`  
		Last Modified: Fri, 17 Apr 2026 00:22:50 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6bee42b5cd9f16a65a4cea96602e32094d92bdd8ffc50be9fdaff9c00845ef`  
		Last Modified: Fri, 17 Apr 2026 00:22:50 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52fec6465bbd70176aa2f55c810d5bd1f47af9118ad57a45fe65dff2b8b255c`  
		Last Modified: Fri, 17 Apr 2026 00:22:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:a374656e46fe5b6cc61bae0ca6f0d947ba59156b4cb988f65d551d22effbc1e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e3ae78d9605040b72853f82c7b479ed37cdf26e71167d3db123c083469389f`

```dockerfile
```

-	Layers:
	-	`sha256:d5711e6ac4caf1c5eabc8790f4209f55e2922c89a72a04160802151e61ebe405`  
		Last Modified: Fri, 17 Apr 2026 00:22:48 GMT  
		Size: 596.3 KB (596347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3c724004067767f0f0cc0a42aec259e91e685a67b814714efe09c968ad60549`  
		Last Modified: Fri, 17 Apr 2026 00:22:48 GMT  
		Size: 43.9 KB (43884 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:5ef264ef2417f35a900a6b12c2af69f2b0770d9aeeebec458a644213a607bf41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115737015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ae02924930ae4e60d9234e0a814c9eefd01aa227f59ea146bf40f261cdcb65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:19:42 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:19:46 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:19:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:19:46 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:19:46 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:19:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:19:46 GMT
ENV PG_MAJOR=16
# Thu, 26 Feb 2026 19:19:46 GMT
ENV PG_VERSION=16.13
# Thu, 26 Feb 2026 19:19:46 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Thu, 26 Feb 2026 19:19:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:22:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:22:03 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:22:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:22:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:22:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:22:03 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:22:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:22:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:22:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:22:03 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:22:03 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:22:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1c3f9d53834e835a762ee5b67b6079af62dd548622f4d26f76355f6fda020a`  
		Last Modified: Thu, 26 Feb 2026 19:22:18 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537ee61db09846e13b7444462cd70783b6b20f75ca89fb810a853f87d2b31e55`  
		Last Modified: Thu, 26 Feb 2026 19:22:19 GMT  
		Size: 890.6 KB (890636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e734bb898c48bd6cd0b74b3cc174aeb5f1e39cb772b190130a290fc0c82dcf`  
		Last Modified: Thu, 26 Feb 2026 19:22:19 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c7257025df7671238dde5512bc2ad4013c8326fd531715e14fa81b2263611e`  
		Last Modified: Thu, 26 Feb 2026 19:22:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad1dbf1b9e7f918d2ab962361b0bd27d5c17da5f9592ffcae34f6e6cea5b8c`  
		Last Modified: Thu, 26 Feb 2026 19:22:22 GMT  
		Size: 111.2 MB (111208443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b715729ca13b6b93a22af9b3dd60c5c4f0d3d8c401ddb27584b5fe2d16d4f351`  
		Last Modified: Thu, 26 Feb 2026 19:22:20 GMT  
		Size: 9.6 KB (9621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e1cd24740282aabfeece1de15aaf1aa2dd5a255edb950226f1268b752ba187`  
		Last Modified: Thu, 26 Feb 2026 19:22:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81018300b59d4a7e42bd2a81f676a93ecbfd966ee5137f2046fce44172a68ecd`  
		Last Modified: Thu, 26 Feb 2026 19:22:20 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a482722963be836a40f4dc0cc67177eb613d95d35c88b22b058a843d3ed27d0`  
		Last Modified: Thu, 26 Feb 2026 19:22:21 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4783f2f96d6dd8fa4f3f7ab264dda9d0a2f338f649ea6d9051e50dbc678ea514`  
		Last Modified: Thu, 26 Feb 2026 19:22:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:dc28ee69f7657a1763fcfb594f43cfbcc5ffad7a18c33c6d07b79868cab6f9c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.9 KB (639945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e01f32c3fe0e55d3b2f71470f1bef9e6a838dc857f2309b835275cf34bb01f`

```dockerfile
```

-	Layers:
	-	`sha256:f59c761b3d3177baf6dc06daca3e3044ae6419688575176887fce0c0efefb7ff`  
		Last Modified: Thu, 26 Feb 2026 19:22:19 GMT  
		Size: 596.3 KB (596300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a2e33339339dc22e305d1b9f5f68159edfd6f450fc061405dac40d09ca22b6`  
		Last Modified: Thu, 26 Feb 2026 19:22:18 GMT  
		Size: 43.6 KB (43645 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:146163cb3f3f547011a3d21527f3f2305646fc888e2b60c97e9dfbf4cad961df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93282419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5164fa39baf13773dd4a7d305e8b081048e75a12cf07d29b742b44ac843f59cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:55:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 17 Apr 2026 00:56:01 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Apr 2026 00:56:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 01:01:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 17 Apr 2026 01:01:39 GMT
ENV LANG=en_US.utf8
# Fri, 17 Apr 2026 01:01:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 01:01:41 GMT
ENV PG_MAJOR=16
# Fri, 17 Apr 2026 01:01:41 GMT
ENV PG_VERSION=16.13
# Fri, 17 Apr 2026 01:01:41 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Fri, 17 Apr 2026 01:01:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 17 Apr 2026 01:05:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 17 Apr 2026 01:05:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 17 Apr 2026 01:05:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 17 Apr 2026 01:05:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 17 Apr 2026 01:05:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 17 Apr 2026 01:05:12 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 17 Apr 2026 01:05:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:05:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 17 Apr 2026 01:05:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:05:13 GMT
STOPSIGNAL SIGINT
# Fri, 17 Apr 2026 01:05:13 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 17 Apr 2026 01:05:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994fd3b166293e4617ca5472a952e8dc21082efd9682a43943df39ebcf544ae4`  
		Last Modified: Fri, 17 Apr 2026 01:01:06 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2b60bc8e7f425f63f0830c9466a974ba3e426f197d170fb82acc065521ab50`  
		Last Modified: Fri, 17 Apr 2026 01:01:06 GMT  
		Size: 878.3 KB (878310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c70dfbaf97c3011265a74c613fd16f2b58f99917b21da4f87f1a93ff3b34dfa`  
		Last Modified: Fri, 17 Apr 2026 01:05:48 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ee1fb225d778c596655a48908ccf2b01fb7422624a9d500fa81bcdff64aa0d`  
		Last Modified: Fri, 17 Apr 2026 01:05:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d9d5ef9f54f0b73e6ecc09a39698cf78b5837204e85680c939b37255b67a3f`  
		Last Modified: Fri, 17 Apr 2026 01:05:51 GMT  
		Size: 88.7 MB (88650233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b956cc5685654aa49542a4b8c5c8b8a7edc67f83ffdee9d570fbe68c8e2be0f`  
		Last Modified: Fri, 17 Apr 2026 01:05:48 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150a7c8e010f64b41ca754c01a7a68c0aa635698ead1dcc383d9db24737dce56`  
		Last Modified: Fri, 17 Apr 2026 01:05:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dec2341980dcce73f1ae374622fd1db0717d5d798fb6b7fa2d70ec86673e13`  
		Last Modified: Fri, 17 Apr 2026 01:05:50 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d21495cd8fed8a789216cdd36cd1aa0acf2860bee5d6a5b2e45d37c9525d27`  
		Last Modified: Fri, 17 Apr 2026 01:05:50 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ead0cca866eff3e63d6677dc02f3fee331788591dc3231b6309984ec9b41ed0`  
		Last Modified: Fri, 17 Apr 2026 01:05:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:d9634b15a4080ea81d068e725353b429127533eec6764436bf1bbae30b8463b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.4 KB (636449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a82667f223292dc4fbfa8e9f56874eb17d967ce13baed09993b08ead004e34f`

```dockerfile
```

-	Layers:
	-	`sha256:e09c2fa973469e88244ddb6c5124f2d8801ca8ecffb162b75dc0e1eef59afd91`  
		Last Modified: Fri, 17 Apr 2026 01:05:48 GMT  
		Size: 592.7 KB (592724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95bcebe50e0bfe4edbb35b9efe530cc3fcec13d6bba0f2f9a3dda2734dffe4ac`  
		Last Modified: Fri, 17 Apr 2026 01:05:48 GMT  
		Size: 43.7 KB (43725 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:7fb9e93550c4646f06a5b51aa6ebbfaaf0883b215eb1ca660dfedaea6f764bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109506865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517f1670d776e21ca23c66c25fb9b52adf089088814afb1712f32c83ddf185cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Fri, 13 Feb 2026 00:03:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 13 Feb 2026 00:03:22 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Feb 2026 00:03:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Feb 2026 08:02:34 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 13 Feb 2026 08:02:34 GMT
ENV LANG=en_US.utf8
# Sat, 28 Feb 2026 10:59:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 28 Feb 2026 10:59:41 GMT
ENV PG_MAJOR=16
# Sat, 28 Feb 2026 10:59:41 GMT
ENV PG_VERSION=16.13
# Sat, 28 Feb 2026 10:59:41 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Sat, 28 Feb 2026 10:59:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 28 Feb 2026 11:49:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 28 Feb 2026 11:49:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 28 Feb 2026 11:49:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 28 Feb 2026 11:49:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 28 Feb 2026 11:49:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sat, 28 Feb 2026 11:49:10 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 28 Feb 2026 11:49:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 11:49:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 28 Feb 2026 11:49:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 11:49:10 GMT
STOPSIGNAL SIGINT
# Sat, 28 Feb 2026 11:49:10 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 28 Feb 2026 11:49:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9a8d29c18a7aa35e1e673e585403324e4011c659e3a9af9631eeef53eb1abe`  
		Last Modified: Fri, 13 Feb 2026 00:55:28 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f6ced6daa9dca5801962fab9724b150e63d0b23f3667a8a57104fdc08d51d`  
		Last Modified: Fri, 13 Feb 2026 00:55:28 GMT  
		Size: 866.6 KB (866630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fefaa019570f036a479949adc1cff90d83d62dfcccda924ecbc9fb276d79751`  
		Last Modified: Fri, 13 Feb 2026 08:54:08 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a21a3b98c9b6bafb53cc153f92fb4167f502f246a409bab23715b2cfca06be`  
		Last Modified: Sat, 28 Feb 2026 11:51:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796ca2d496a47dc28ad39f0c896252742d00a40753e77aa890594162deebfb30`  
		Last Modified: Sat, 28 Feb 2026 11:52:16 GMT  
		Size: 105.1 MB (105105596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10e23418e9be03c336d9e5342af0e1078053747f034e4702d43fb9cedb8003f`  
		Last Modified: Sat, 28 Feb 2026 11:51:59 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5789cf208c3583eee4af9ea2d89ce6976fe7137bf8ba88d8ca4e2de74abd1775`  
		Last Modified: Sat, 28 Feb 2026 11:51:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc0dae68f2f858079d5124971ade1c1f94133ae9e475f29fa8de508074a357a`  
		Last Modified: Sat, 28 Feb 2026 11:52:01 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ee03ddbde2568a7ea61a30ed8d551179a69cd490c19a78d1ce0f394bf5b991`  
		Last Modified: Sat, 28 Feb 2026 11:52:00 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcfd556823c9819bfb859328acc37c1bdd9b859c72ba23640d76066f70d5af7`  
		Last Modified: Sat, 28 Feb 2026 11:52:01 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:4f768d05907e64214e4fd05a88fb3f58a0486e3f206b925fc519dcda27441ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.1 KB (638114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70e4021d88f9bb957e76beb55e9e02dcfa1c61c796faf1e4aa27b49cb581491`

```dockerfile
```

-	Layers:
	-	`sha256:7ff96d1b2aba883986e1bf54beac4b1eb7d10375edee851b8bef1a94cef548c9`  
		Last Modified: Sat, 28 Feb 2026 11:51:59 GMT  
		Size: 594.4 KB (594382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cb35ac3963b0b4129709687f24361d5b6beaf46348e3143fbf02e6bdfdbd6eb`  
		Last Modified: Sat, 28 Feb 2026 11:51:59 GMT  
		Size: 43.7 KB (43732 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:09d7696672295e31bee36de30720f4b87c9b4c3453928bb03ee7bd1fb19e42ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118202714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370fd1d116f4cf8589740ec8ba9b7281cb54753cef5490e2be980af99f9d77b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 17 Apr 2026 00:32:18 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Apr 2026 00:32:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 00:32:19 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 17 Apr 2026 00:32:19 GMT
ENV LANG=en_US.utf8
# Fri, 17 Apr 2026 00:32:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 00:32:19 GMT
ENV PG_MAJOR=16
# Fri, 17 Apr 2026 00:32:19 GMT
ENV PG_VERSION=16.13
# Fri, 17 Apr 2026 00:32:19 GMT
ENV PG_SHA256=dc2ddbbd245c0265a689408e3d2f2f3f9ba2da96bd19318214b313cdd9797287
# Fri, 17 Apr 2026 00:32:19 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 17 Apr 2026 00:36:36 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 17 Apr 2026 00:36:36 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 17 Apr 2026 00:36:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 17 Apr 2026 00:36:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 17 Apr 2026 00:36:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 17 Apr 2026 00:36:36 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 17 Apr 2026 00:36:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:36:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 17 Apr 2026 00:36:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:36:37 GMT
STOPSIGNAL SIGINT
# Fri, 17 Apr 2026 00:36:37 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 17 Apr 2026 00:36:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291c16c7ab912f2d58c247613c580206f937282696d32e38ceeb3c6160e7da86`  
		Last Modified: Fri, 17 Apr 2026 00:37:03 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f52ee6117c4125eb05dc2cc4439c5034b513216f81be4e75482999870021cd`  
		Last Modified: Fri, 17 Apr 2026 00:37:03 GMT  
		Size: 894.2 KB (894236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608128b344af24b94dc14b0137394ae13b024a26c5ac23f4ffeeb40527859464`  
		Last Modified: Fri, 17 Apr 2026 00:37:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73da819c09b55320485ba81daf276951c1f9876e56e6459f0274232bd5f481d8`  
		Last Modified: Fri, 17 Apr 2026 00:37:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beb4cea7248614be1beb68990a3385d0da9da11bd4cb6c50ef44127bf987d61`  
		Last Modified: Fri, 17 Apr 2026 00:37:06 GMT  
		Size: 113.6 MB (113637400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f676e329f5f1568f5b7c347c759f371c07112d0706bf5167d70727f0ecb0bcd`  
		Last Modified: Fri, 17 Apr 2026 00:37:04 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6578285c304205a344dfcedd31c7d75a7c61c162d3e56ca38c724e05125f5f0`  
		Last Modified: Fri, 17 Apr 2026 00:37:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4953e809e2a9adcd8a381a4df47e369a89249f2bbdc49452350ac516ffd7122`  
		Last Modified: Fri, 17 Apr 2026 00:37:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4acd9831d94af93e642711ec56c05e57418e1e8fe38a404b3499eb4143a0f61`  
		Last Modified: Fri, 17 Apr 2026 00:37:05 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8a296c1d7dc50bcefa542f465bcce5431533b07be6fff9dd62a9f1bb2d93fd`  
		Last Modified: Fri, 17 Apr 2026 00:37:05 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:60558d2615bef214afe23411b22c1650b6e76eba201973b3003efd5b64c7e9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.0 KB (638048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b1b1c7badc8d372c3bf0db7faeb9c1540d162a123a6da10a53edd381fb5557`

```dockerfile
```

-	Layers:
	-	`sha256:5a028290793e0174d3119b4229d57a2384d326ccb3d23721bdf4d7b4ddec2a58`  
		Last Modified: Fri, 17 Apr 2026 00:37:03 GMT  
		Size: 594.4 KB (594364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:454d3a9ae97e17f6f2647d043e2e458d9fef94caca8751cb48dbe485cd055e6b`  
		Last Modified: Fri, 17 Apr 2026 00:37:03 GMT  
		Size: 43.7 KB (43684 bytes)  
		MIME: application/vnd.in-toto+json
