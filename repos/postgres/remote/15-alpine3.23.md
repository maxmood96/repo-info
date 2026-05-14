## `postgres:15-alpine3.23`

```console
$ docker pull postgres@sha256:2a6577fca547b9021b9281c58bc71ec1617e05b8d128c8875bd5fa32c267c554
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
$ docker pull postgres@sha256:f9cbc643bd3ae158a48241527e5306cdbd9958cbf65c09842770e564f5ff686e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109190422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cce759a2777634ff1edd0d56b9241a2961deb7f72e125d4af6ae2928163a6b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 19:02:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 19:02:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 19:02:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:02:17 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 May 2026 19:02:17 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:02:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:02:17 GMT
ENV PG_MAJOR=15
# Thu, 14 May 2026 19:02:17 GMT
ENV PG_VERSION=15.18
# Thu, 14 May 2026 19:02:17 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Thu, 14 May 2026 19:02:17 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:04:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:04:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:04:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:04:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:04:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:04:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:04:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:04:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:04:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:04:09 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:04:09 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:04:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabfbb74125319d539256c118ba590e5960ede5003533eddd871e5d0394985a9`  
		Last Modified: Thu, 14 May 2026 19:04:23 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7083820709061e16227030a4650686e84171a0270750095ec45ebfe6ad4f6c`  
		Last Modified: Thu, 14 May 2026 19:04:23 GMT  
		Size: 919.1 KB (919067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8a2f657a653e2ab7ba51273b2ef85a760c502cf93025336380e62dd09bbca6`  
		Last Modified: Thu, 14 May 2026 19:04:23 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba0314f1de5eb76378789ce66ec8efa3276242ed12ad823ea9d72e5aefa881e`  
		Last Modified: Thu, 14 May 2026 19:04:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875febe691e3833a74a4b2c3267083feb7f9c26036c1ab3e58d19f50ff57a743`  
		Last Modified: Thu, 14 May 2026 19:04:27 GMT  
		Size: 104.4 MB (104389877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5aa5cfeb581c0dab162dcb611a85bf4f122fbc46d692d173950417876d1dcfa`  
		Last Modified: Thu, 14 May 2026 19:04:24 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d16d98c9e28586c688b967827f0d116c31fd249b34099420f710b07d2c327c`  
		Last Modified: Thu, 14 May 2026 19:04:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089c22c5ccd159cd3911304f5236b25dd6f0a5b40414c801836031a1428e2847`  
		Last Modified: Thu, 14 May 2026 19:04:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2cc7995f675f58240a1e474679f0b5526207aaae6c64486bffb7c1ff453014`  
		Last Modified: Thu, 14 May 2026 19:04:25 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7388fabcfc89f10db0b1e45bf16fa23e9a20cb779207a564d241ecaaa87d617`  
		Last Modified: Thu, 14 May 2026 19:04:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:de64486e0b79a201551913148e4c27120f0ae55a54cc9e76ff66f644a4c483b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.5 KB (642498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a693285844a27341fddf92c3354e0c9f0659a3a0cd75a69b829c145c51b05812`

```dockerfile
```

-	Layers:
	-	`sha256:c8e31ffa020754eb4e908ed1259bb14886ed4371f28795804509360ada7aa1c1`  
		Last Modified: Thu, 14 May 2026 19:04:23 GMT  
		Size: 598.1 KB (598108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd9452a9126c62042efac142fc3193066da1ff9d4c230e0f37c9199781ddda1`  
		Last Modified: Thu, 14 May 2026 19:04:23 GMT  
		Size: 44.4 KB (44390 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; arm variant v6

```console
$ docker pull postgres@sha256:01f75f240642a949b1a940c3b98b8398c230bdcdac904da3468fae77fa9bee85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88672768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa0e057343497d6c1a9a824a2179d51283b2e40006820a05373fa9c453002c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 19:14:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 19:14:47 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 19:14:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:18:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 May 2026 19:18:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:18:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:18:20 GMT
ENV PG_MAJOR=15
# Thu, 14 May 2026 19:18:20 GMT
ENV PG_VERSION=15.18
# Thu, 14 May 2026 19:18:20 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Thu, 14 May 2026 19:18:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:24:21 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:24:21 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:24:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:24:21 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:24:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:24:21 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:24:21 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:24:21 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:24:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:24:21 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:24:21 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:24:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637a627c731ce99fd395eae325f414ac628a21224f4f84394d47511af44aacad`  
		Last Modified: Thu, 14 May 2026 19:18:07 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b600a6745f9fa98fad09d777607236c9591b17dfd9824aacfc3dc21239bc7e0b`  
		Last Modified: Thu, 14 May 2026 19:18:07 GMT  
		Size: 887.1 KB (887120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6927de5daf8edc7e2d2a6aee190d01918bb70549f8e72c31daf31a03929c9a6c`  
		Last Modified: Thu, 14 May 2026 19:21:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd23fbf4f2d6ee9dfb45901c40ddcdcba24e906b6ce25a20b6a476f0f50f7a6`  
		Last Modified: Thu, 14 May 2026 19:21:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4903bc7607b7815db9aabdf42d8d270edcb01bf65bed91f4ce2cfdacf14b4a8f`  
		Last Modified: Thu, 14 May 2026 19:24:34 GMT  
		Size: 84.2 MB (84196498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad12c567018d30285fd9fac4861102ca62b1ea3d42443740ddc9266b6e218747`  
		Last Modified: Thu, 14 May 2026 19:24:31 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672b7c9023d2620ca101c8d9ba2c3ea6210f8e502fac4f77db323e7e6df8cd25`  
		Last Modified: Thu, 14 May 2026 19:24:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7d4a75a2bbbc738ad70fe8caa7a53193e81ceb1dafa4daedd28216e833873e`  
		Last Modified: Thu, 14 May 2026 19:24:31 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0fee29834483f983d395fafd874e1c52373fea80cf14c7af8405b76d4a1abb`  
		Last Modified: Thu, 14 May 2026 19:24:32 GMT  
		Size: 6.1 KB (6093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb006a9c65dcda2719b8a3a4faa6d672f9a934b81ccf26f399b123209f31320`  
		Last Modified: Thu, 14 May 2026 19:24:33 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:9183a566221b34f15124ce6c8ea22f20b7dfbe80b603587ef44fff1277c01137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 KB (44353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4113ad1e53036e6ab20a53fddc1bdcd63cff336f51c11d05741def74f5f20f8`

```dockerfile
```

-	Layers:
	-	`sha256:4a8120fc29738574910e35abadca2e63a3f7037dec3f054c8a75be3004df1cdc`  
		Last Modified: Thu, 14 May 2026 19:24:31 GMT  
		Size: 44.4 KB (44353 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; arm variant v7

```console
$ docker pull postgres@sha256:35efbdf4acacd32c24b173f7051c9678d50342a0cec634242aa4f802bf1fd7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83916925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1ed3eae87b540f06cf440ee72d2e5d2c1a201ab39593205b6943d6cd53654f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 19:27:27 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 19:27:31 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 19:27:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:27:31 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 May 2026 19:27:31 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:27:31 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:27:31 GMT
ENV PG_MAJOR=15
# Thu, 14 May 2026 19:27:31 GMT
ENV PG_VERSION=15.18
# Thu, 14 May 2026 19:27:31 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Thu, 14 May 2026 19:27:31 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:30:11 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:30:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:30:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:30:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:30:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:30:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:30:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:30:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:30:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:30:12 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:30:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:30:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bcaea378e73bca19522ba9d84af4cac166d7b4fd213adf7235e9fcdb569340`  
		Last Modified: Thu, 14 May 2026 19:30:23 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d19a3589c6dfc3afc4aeaa287852f5d26ee514d6dc6e508c1a09e6486a3f69`  
		Last Modified: Thu, 14 May 2026 19:30:23 GMT  
		Size: 887.1 KB (887122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f477e77d6e8e605de3d903f675659bc6bda43348e0e53c9d217a95517772b87`  
		Last Modified: Thu, 14 May 2026 19:30:23 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a182edc893853dc56288020ef9a983ee358d0cb90a4f4778e14dcacb46d7e827`  
		Last Modified: Thu, 14 May 2026 19:30:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d61da1e4f8b998c37ecb6180d61e3a7d25dce1058fbcd6f4573ccccde316c11`  
		Last Modified: Thu, 14 May 2026 19:30:26 GMT  
		Size: 79.7 MB (79729394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8971a7671f3c3b7c0b42a2d6d05c35b62b965db2c5a5d3622a1f0fa5ad647d36`  
		Last Modified: Thu, 14 May 2026 19:30:24 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c92fe523c23902de74d97354d92c195da3c7d6102ca9cfb2634ea3109e0c76`  
		Last Modified: Thu, 14 May 2026 19:30:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25b419e53f96412821d5e46fbe858b7363f772713a31d1ee69654b7fd8b8f42`  
		Last Modified: Thu, 14 May 2026 19:30:25 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edd363da7564de93443b97a1ee2140de2772160074dd6e7a73c87228f0510e3`  
		Last Modified: Thu, 14 May 2026 19:30:25 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de8499ec9c9d1be04334ae02c1c3e0f9df00daab809b2949191d96efe3470b6`  
		Last Modified: Thu, 14 May 2026 19:30:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:90ba2b2d927a85c62d8de1ac4bf85747e32124b8839c71af63765ce042d462a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.1 KB (642062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c1f4990258728ab99123a05636509e2fc566a7a471b6fa15a8c5dff965a283`

```dockerfile
```

-	Layers:
	-	`sha256:1420112bbb3c90af7deec6223ad60e6328cd214cdcd88e2f151c9af3ef5252ba`  
		Last Modified: Thu, 14 May 2026 19:30:23 GMT  
		Size: 597.5 KB (597494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c24c9d0b5c6f5cd7be0a7e3cfd2c01f9b067da2e10daeb0b3a9831f61c1b0a1`  
		Last Modified: Thu, 14 May 2026 19:30:23 GMT  
		Size: 44.6 KB (44568 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:ad551215ec961af6fb03fe68a4ac45390c69a25efd8d20f8730ca0ec5d3b89f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107391570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c4c0fadf81bfe6e93068a06a6810355e5b9909ae5092788d8aa17ee9d8f10e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 18:59:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 18:59:44 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 18:59:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 18:59:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 May 2026 18:59:44 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 18:59:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 18:59:44 GMT
ENV PG_MAJOR=15
# Thu, 14 May 2026 18:59:44 GMT
ENV PG_VERSION=15.18
# Thu, 14 May 2026 18:59:44 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Thu, 14 May 2026 18:59:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:01:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:01:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:01:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:01:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:01:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:01:58 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:01:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:01:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:01:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:01:58 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:01:58 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:01:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c50a26d8508a0e11142660746532b6aa981014ca41bf7da9f146cac4af0500`  
		Last Modified: Thu, 14 May 2026 19:02:12 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db7979f17065bc1677a4fde5ee39390ec5f38ce1d4e3a95cab55bfea97022e3`  
		Last Modified: Thu, 14 May 2026 19:02:13 GMT  
		Size: 874.7 KB (874716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd1b81bc00b60a1fb8daef68298f4ac57bf0e2e44b42841be5b2ee537fe3213`  
		Last Modified: Thu, 14 May 2026 19:02:12 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a808f2c87b42738b6bed53c8ac1f04ef5b18143f6e3dd0b8d8f442e1a3874f6`  
		Last Modified: Thu, 14 May 2026 19:02:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120167562959bfe8a643d2e7ae1813d55c6584a1bea528a131ec8df92183cd0b`  
		Last Modified: Thu, 14 May 2026 19:02:17 GMT  
		Size: 102.3 MB (102299696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2a3eb8444b0d54918145b63a14fa8cba540c01575c6232d8dbc0e9386d05b5`  
		Last Modified: Thu, 14 May 2026 19:02:14 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1601785f803e0ce57b5e6930f7f255462fe146c3e6e782faa3192ab56a1e15`  
		Last Modified: Thu, 14 May 2026 19:02:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff68b9d7626fa87affa61f6e1d5fdb5e4a62657cfd0be2ce9609e45391505205`  
		Last Modified: Thu, 14 May 2026 19:02:14 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3b8203615e6de6eef6d63a169c88c2610608db51801433f17cc67f3e06c8e1`  
		Last Modified: Thu, 14 May 2026 19:02:15 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff61456705de261657aae08235d0aee7acb8a53f13938a0eea5ec5c773625da3`  
		Last Modified: Thu, 14 May 2026 19:02:15 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:84a2ecd408d76019f4a8cd1885107fa4fafd5925746cd352efa022d705e40370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.1 KB (642128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ee6cb9358945e4fca00dbbe60f868470626ea3c7b48f6053a52c7181e8a4f8`

```dockerfile
```

-	Layers:
	-	`sha256:48a2bdeae7fadb282160b087c296a023fab342e8ca3cdbd114ffa559392541fd`  
		Last Modified: Thu, 14 May 2026 19:02:13 GMT  
		Size: 597.5 KB (597514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaa78964148f0e61846fdf83bd1b6cc0d990e2b92ad4b8264a703d4e23906314`  
		Last Modified: Thu, 14 May 2026 19:02:12 GMT  
		Size: 44.6 KB (44614 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; 386

```console
$ docker pull postgres@sha256:84c1bdf2bade26b28449a56771870c7cb8f4f1a6185f127df3701f527d16fd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115252356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797b975503e3e3be0a473c0c24adec1cd72d6d46e3da5b138126d1f2e52362bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 18:58:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 18:58:42 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 18:58:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:02:02 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 May 2026 19:02:02 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:02:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:02:03 GMT
ENV PG_MAJOR=15
# Thu, 14 May 2026 19:02:03 GMT
ENV PG_VERSION=15.18
# Thu, 14 May 2026 19:02:03 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Thu, 14 May 2026 19:02:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:07:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:07:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:07:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:07:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:07:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:07:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:07:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:07:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:07:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:07:40 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:07:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:07:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07229531d7e80aaa1c60635f99b81feb88cddc54f6d0086181b6917a2e4c0768`  
		Last Modified: Thu, 14 May 2026 19:01:53 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27aa7902d75e45f511b751c6737142228cd7f77c10ec9f991166bbb0e9739dd`  
		Last Modified: Thu, 14 May 2026 19:01:53 GMT  
		Size: 891.7 KB (891651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39027f05dcc1d66a6fc65779b8aed16932839f554f0ce0a1a26869f33ae766a8`  
		Last Modified: Thu, 14 May 2026 19:04:58 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40cae4db464fcf92301f63be097d4d3ecce9fc3a220086607c80ae47a316540`  
		Last Modified: Thu, 14 May 2026 19:04:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91db010cbdea31c9b3c9013cf70420fa6a7df1e78c53ccf201b230d266329aa6`  
		Last Modified: Thu, 14 May 2026 19:08:00 GMT  
		Size: 110.7 MB (110652965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad457697ff6980f6aa07ec4c22e62baab3fa1875a92e9975c28726c1002b9760`  
		Last Modified: Thu, 14 May 2026 19:07:57 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c580700a6ba12428971fd8d1d5857dd22d98d4fcbca0e627b061a030825ddfc`  
		Last Modified: Thu, 14 May 2026 19:07:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc879a3c1719169a09662d137bcbd56679ecf93981ee2e1119efdc5f3f0584`  
		Last Modified: Thu, 14 May 2026 19:07:57 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c0cf927d6d1342b2e669207c7f7a724a5a41190e9c1a03b42481fba17adb0b`  
		Last Modified: Thu, 14 May 2026 19:07:58 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4beaea42e2e6e7a0dc1cabb0ff01d8b8712f95befbd14de397e8a1ac566c196`  
		Last Modified: Thu, 14 May 2026 19:07:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:07404e107f2671c9fc49d6bccd7782e70c6e3448ce845649729c49a8fe3afb20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42750941364ea325625f083157a9c836a5b59b16cc2b0ee3e136d7d550f9687d`

```dockerfile
```

-	Layers:
	-	`sha256:6d1c099de5863cc858ae9303004289452e62f1a6433d627cb5948bc63a74c806`  
		Last Modified: Thu, 14 May 2026 19:07:57 GMT  
		Size: 598.1 KB (598083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94edf26f29c613ea3ad830146d4d9db97b4e40d87f3e47828df7f1db4e737053`  
		Last Modified: Thu, 14 May 2026 19:07:56 GMT  
		Size: 44.3 KB (44341 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; ppc64le

```console
$ docker pull postgres@sha256:cc734358850edc988ac1672a90709d224903c9dd725a99bf2f7d6098f64f244f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94083382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4849f0d0ba517481c5290de57ccd4b2a9437306b0583944ca14d17db079746a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 18:59:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 18:59:16 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 18:59:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:41:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 May 2026 19:41:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:41:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:41:39 GMT
ENV PG_MAJOR=15
# Thu, 14 May 2026 19:41:39 GMT
ENV PG_VERSION=15.18
# Thu, 14 May 2026 19:41:39 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Thu, 14 May 2026 19:41:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:50:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:50:38 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:50:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:50:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:50:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:50:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:50:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:50:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:50:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:50:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:50:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:50:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef79b67da8e2ac0b3216e1be8c0fdb606b51ba383c9b0bb853e51567459542b`  
		Last Modified: Thu, 14 May 2026 19:39:55 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6954ef680ac898f1adc16c44963bcb8ba30fdf4ab7575d8eddf11a33a3513315`  
		Last Modified: Thu, 14 May 2026 19:39:56 GMT  
		Size: 880.1 KB (880131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826dd44db94078537abd2198b92a58561d03c73b8089972a256864ea059c2300`  
		Last Modified: Thu, 14 May 2026 19:45:28 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9503d05c783ed3a14946a64ab5da87eedf80210e862939e579905433695a3e2f`  
		Last Modified: Thu, 14 May 2026 19:45:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829c43d25316e049c9e574bad953139915394c511068e84ddcbf1ad027350348`  
		Last Modified: Thu, 14 May 2026 19:51:08 GMT  
		Size: 89.4 MB (89355026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba27ae8ed28060a4842262f2076ffea8f3947ae4c06bd0a302fff2662e96d7a9`  
		Last Modified: Thu, 14 May 2026 19:51:05 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5751986a8fdffaedf41cc30c2fe5a7a5e990f2d10fccc46d4532a5899e4a1f0`  
		Last Modified: Thu, 14 May 2026 19:51:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275542af7d535a7e3ca2cdb9fba3f14cb8d60ffedf8bdc2c0ec4353f4cae8550`  
		Last Modified: Thu, 14 May 2026 19:51:05 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c536dadbd3e2c52d8dc98ac4216dc68e181ded87e4207574093994e62c24db64`  
		Last Modified: Thu, 14 May 2026 19:51:07 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b39b88a78b3a4e230dc7fced1c7d3b07da156bec6205a7a0acfc9d0ce6e3b55`  
		Last Modified: Thu, 14 May 2026 19:51:07 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:8008f6d05a15e02a7f11bb4772c586e1b84821b9051f2742701c620dd91b83d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.3 KB (640273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0113a4becc2ffa35f93557252e8bb28a1a074f2084aa887b68961e3af8246590`

```dockerfile
```

-	Layers:
	-	`sha256:df848827788881585d211eea424de3e6f8ac0f3d8f627bf1f3ce36b60975d231`  
		Last Modified: Thu, 14 May 2026 19:51:05 GMT  
		Size: 595.8 KB (595829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c69dd2618e0422d51d943ada89430187206566c873812ee7a1b7a2ed556f5a97`  
		Last Modified: Thu, 14 May 2026 19:51:05 GMT  
		Size: 44.4 KB (44444 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; riscv64

```console
$ docker pull postgres@sha256:02ae7eb3b2f4ba82e495729a6b102e1e0e450474c2b197a0dc827043d131e30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.2 MB (110150131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d40a86ac7253524aa04f068a11282e53a3c6f4302e6b0369dd93d703070108`
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
ENV PG_MAJOR=15
# Thu, 16 Apr 2026 13:20:59 GMT
ENV PG_VERSION=15.17
# Thu, 16 Apr 2026 13:20:59 GMT
ENV PG_SHA256=ae14f24c14727e0b2ded1c5553031666099bd1054db3ef44bfa6e2bd6d554a56
# Thu, 16 Apr 2026 13:20:59 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 16 Apr 2026 15:03:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 16 Apr 2026 15:03:49 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 Apr 2026 02:45:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 22 Apr 2026 02:45:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 Apr 2026 02:45:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 22 Apr 2026 02:45:03 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 Apr 2026 02:45:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:45:04 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 02:45:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:45:04 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 02:45:04 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 02:45:04 GMT
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
	-	`sha256:be77d9005e33b8f3c5ea64fb271b287c255adc6232163e9fb6db86d552dd3a98`  
		Last Modified: Thu, 16 Apr 2026 15:06:49 GMT  
		Size: 105.7 MB (105677621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a953d9684a69a9292146d40197d4a61262ed078f4010121aa73f1d50c785cfb4`  
		Last Modified: Thu, 16 Apr 2026 15:06:34 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45140c8273adaefe8fdc5435b2183c70b41d90bf1e1f892eb8ccf28be6376b1a`  
		Last Modified: Wed, 22 Apr 2026 02:46:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f958902e7ca670c092691aa8d5128ed95b30221e4084fd0b2fd0ffd4d6bdf5b`  
		Last Modified: Wed, 22 Apr 2026 02:46:19 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9636779a612a90791b8830f1de3685fb38018eca44d49310a4a16ef8706d1635`  
		Last Modified: Wed, 22 Apr 2026 02:46:19 GMT  
		Size: 6.1 KB (6104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694f33694765f2c8decef3ed5dca0c8502a202c9035eac30e480f4c964ad785b`  
		Last Modified: Wed, 22 Apr 2026 02:46:19 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:581e8a6597abf8ae76aa3ff683a72e25eee67abc8b66093f235541fe9067a1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.9 KB (641937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f2ff877fab78080041cde337a5419a2f2114d012fd3bffd609b75612e6b938`

```dockerfile
```

-	Layers:
	-	`sha256:a1d766cd1b346303dc533490b91b1d145c5a85fc205414879a13e201af5b1d2a`  
		Last Modified: Wed, 22 Apr 2026 02:46:18 GMT  
		Size: 597.5 KB (597487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8651ff31b226912991a94066d6e24df5aa4679d864f88388ab670d2fcbdce2f`  
		Last Modified: Wed, 22 Apr 2026 02:46:18 GMT  
		Size: 44.5 KB (44450 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.23` - linux; s390x

```console
$ docker pull postgres@sha256:c13d265155acff9d468c51db159554d629dca04804477157d61a65aeb1d45d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117345948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99c6a3a70a910ad781e5109a473f42389470f61428d4889bdf0caa10137671f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 19:26:54 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 19:26:56 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 19:26:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:26:57 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 May 2026 19:26:57 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:26:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:26:57 GMT
ENV PG_MAJOR=15
# Thu, 14 May 2026 19:26:57 GMT
ENV PG_VERSION=15.18
# Thu, 14 May 2026 19:26:57 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Thu, 14 May 2026 19:26:57 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:29:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:29:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:29:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:29:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:29:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:29:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:29:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:29:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:29:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:29:44 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:29:44 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:29:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7becaf45a4240c96f6c0d87fcb78679b0b53a52d9939692b897b9441599bf27a`  
		Last Modified: Thu, 14 May 2026 19:30:08 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415320e1528c7f77dbf381e4a7ccda7f15c6fabe8bed8fb04b94aff32a085e0e`  
		Last Modified: Thu, 14 May 2026 19:30:08 GMT  
		Size: 895.8 KB (895809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2a3938d6360ebc1543c6260cf969b98fdfb27ffa6176b66605d73c0d910ff8`  
		Last Modified: Thu, 14 May 2026 19:30:08 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d50d5cd7211fa48da46535ae1a0100cd39034b4d9d8c0e5279fe76130d5137`  
		Last Modified: Thu, 14 May 2026 19:30:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcfaf48067311184f0fe3da3318bf85554417cb8db1738c5b3a6bf307c877bd`  
		Last Modified: Thu, 14 May 2026 19:30:11 GMT  
		Size: 112.7 MB (112706322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7131c7173c0840d73864ade3d21e383d5f9830a5863d20d28c5da94cb94eaa4`  
		Last Modified: Thu, 14 May 2026 19:30:09 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8aae9ce7fa0f1748cd2fd1a26a0bc728375876877a6270411637cdd4287e80`  
		Last Modified: Thu, 14 May 2026 19:30:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df74a432ebddc3947e2aacf696507d96963ee814d7dd9e0e359662cec5768cb`  
		Last Modified: Thu, 14 May 2026 19:30:10 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3ef8c69460f6c411a17d2af95946f240239048939c0eaaa9d875948a2d39f5`  
		Last Modified: Thu, 14 May 2026 19:30:10 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7ad05da099eeaabf179c4e51575c4de7c275595ffc3a9fe8c6c559a0adf499`  
		Last Modified: Thu, 14 May 2026 19:30:10 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:aa7157ca8c4e86514d86a99bbea3a159bd408ddd5410459adc288060969d2b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.8 KB (641847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafcc42a0efbaf6b108cc2c0eb855b58a5bfee6f078034b9c3e15ec588ea5517`

```dockerfile
```

-	Layers:
	-	`sha256:5ae0445844c34b2332ed5e02b1daec77fc03a922473dab6d2641981366c4599b`  
		Last Modified: Thu, 14 May 2026 19:30:08 GMT  
		Size: 597.5 KB (597457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52f8375925f7db818da309e20aafb8b17b074e0106a96c178089ef526e2dc5ce`  
		Last Modified: Thu, 14 May 2026 19:30:08 GMT  
		Size: 44.4 KB (44390 bytes)  
		MIME: application/vnd.in-toto+json
