## `postgres:15-alpine`

```console
$ docker pull postgres@sha256:cd17e2ac98240fce1541ad2a803b34009b4eea5aec8a832363cdc7eca62e722e
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

### `postgres:15-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:878ac61a6367f60973ed0eef22ade9956e075f1a21f4604867e33a2edb6939e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115195174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9943612906a85ac94fc483581457e28bd13a424e0e0fceb0499a81f058e53c81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:59:45 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:59:47 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:59:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:59:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 22:59:47 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:59:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:59:47 GMT
ENV PG_MAJOR=15
# Tue, 16 Jun 2026 22:59:47 GMT
ENV PG_VERSION=15.18
# Tue, 16 Jun 2026 22:59:47 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Tue, 16 Jun 2026 22:59:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:02:02 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:02:02 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:02:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:02:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:02:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:02:02 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:02:02 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:02:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:02:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:02:02 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:02:02 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:02:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc76471c3c7fda49e7e9816fa48ae136f0b46d7ccb9e47aec490f372ebd8039`  
		Last Modified: Tue, 16 Jun 2026 23:02:19 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5bf1ac61638fbe78a9340440c9c0c444e4d4037b5cb421e800b19611f4e43f`  
		Last Modified: Tue, 16 Jun 2026 23:02:19 GMT  
		Size: 900.3 KB (900258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853349fea82d9f25f9baa4cb0cbbfce0bc3dc9e217aa05d6e6af4faeaa6303b5`  
		Last Modified: Tue, 16 Jun 2026 23:02:19 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5e85922300e5eb086371742b4c3463c382fdc392f08db6b131e49a20b4735f`  
		Last Modified: Tue, 16 Jun 2026 23:02:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4608fab9e71253478ccbc28a07298bce30caa8ff8b3a4cdc383de1d6e7490454`  
		Last Modified: Tue, 16 Jun 2026 23:02:24 GMT  
		Size: 110.4 MB (110431238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e56b5bebbf4f69882a7874870c2cc340d3ce9875eabe7d0362f116bd7821aa`  
		Last Modified: Tue, 16 Jun 2026 23:02:20 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e97e707df136535050ef2e85efdde5d4239a2badea0153c2dce151d632884b`  
		Last Modified: Tue, 16 Jun 2026 23:02:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6efd2a4e3d43ecc6a965568478ad843cb49ccbb00a3c722eee60df6780419c8`  
		Last Modified: Tue, 16 Jun 2026 23:02:21 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e385447d2cadf35197cf3b95584b8943a596f874e7b96b86ec22c8e5ebc9da`  
		Last Modified: Tue, 16 Jun 2026 23:02:23 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a354ba7f6e31d8359fd22dd34e189a823df3e47b198851a6a52b0c36b8c1c8`  
		Last Modified: Tue, 16 Jun 2026 23:02:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:170db4a0c99efb5f91c8f87f44785dbab5e2602e7ff6ae7e3b5de2bda50372f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8706fd073c48ebd7cb58b6a9088e539cf8eafe2941f67c5c897ab8fcf1c57331`

```dockerfile
```

-	Layers:
	-	`sha256:6d17d809c137370126b1dd4e96242522a09dc488e6f5f17595b245a2a4f14bd9`  
		Last Modified: Tue, 16 Jun 2026 23:02:19 GMT  
		Size: 598.0 KB (598034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e03b28372d4f83dcbff78e05d02ead9f234ff6cb404a58f5e14efe2bcf780f`  
		Last Modified: Tue, 16 Jun 2026 23:02:19 GMT  
		Size: 44.4 KB (44390 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:055cc3105859ec44be8160a6a13146982d2d6b7b02d49e5d249e0ffbf87563f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111498067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15da30251b14d53c469374004e17948ad3e4ae91e9dd1b49b7d348ff0d80a87f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 23:01:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 23:01:58 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:01:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:01:58 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 23:01:58 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 23:01:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 23:01:58 GMT
ENV PG_MAJOR=15
# Tue, 16 Jun 2026 23:01:58 GMT
ENV PG_VERSION=15.18
# Tue, 16 Jun 2026 23:01:58 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Tue, 16 Jun 2026 23:01:58 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:04:54 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:04:54 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:04:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:04:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:04:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:04:54 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:04:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:04:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:04:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:04:55 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:04:55 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:04:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef29dece8af1a30d8e4604607c6e543496a4e40f4583bd08b1a400682df62f4a`  
		Last Modified: Tue, 16 Jun 2026 23:05:06 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a83966d0f18d0f8b41278fd2fc8cac8f603514adf4e1fe72644936542b9753`  
		Last Modified: Tue, 16 Jun 2026 23:05:06 GMT  
		Size: 864.6 KB (864619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf0ff9d0fd5911b7f7f08e6ef2672f6a215d99cc644bf802e90416892bb3e5a`  
		Last Modified: Tue, 16 Jun 2026 23:05:06 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4394a73b3347e05c7d0dd1103163e35111e09c6f04eb12e1703e1dd8072daac`  
		Last Modified: Tue, 16 Jun 2026 23:05:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9f18cfcbb5b520dd49b2dd1eff87bddbd9c67ccd6a462aa7d023b6f09fe7b`  
		Last Modified: Tue, 16 Jun 2026 23:05:10 GMT  
		Size: 107.1 MB (107062710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd75c481fcebf518d716397de5d5108e0d96cdebdb28e58b943b95f8323247a`  
		Last Modified: Tue, 16 Jun 2026 23:05:08 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061a2164299839d54ea9523d03c8fdf2a145af0a8f30283e86524b4e741c5d56`  
		Last Modified: Tue, 16 Jun 2026 23:05:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363e702f4e928fcaf327c1df5d3198fe115b74cfd49a5d110d48ad1636869f77`  
		Last Modified: Tue, 16 Jun 2026 23:05:08 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7b7f2c3aef059b63a5c023c8f164ce8507c21c4ebd818c8033a78e9fb594aa`  
		Last Modified: Tue, 16 Jun 2026 23:05:09 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27fc81aa4602434f5979972cbf7d1c07c9b755867d8561ea2de6a97f19a05f1`  
		Last Modified: Tue, 16 Jun 2026 23:05:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:4d81957ea678e04a61e55506af190ad39a3de800c932017cca23f2c96e22a284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 KB (44359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89031fd3b6995e2eeacbb9bcca658aaf84976199363ae9e22d48f017f3d06007`

```dockerfile
```

-	Layers:
	-	`sha256:a8127a31ad72995f1b51ab8339623b43fa22ad4669e62169b0fdcf3bbca96dc6`  
		Last Modified: Tue, 16 Jun 2026 23:05:06 GMT  
		Size: 44.4 KB (44359 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:8ec02149e24f16039613f3fd53c4bb16b9b1160f838caab6a4aba7bccec322cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105222788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ec03a6c949cdd502645f2f156d3dbe55ad7f2e173a9a87700d3bd4d649f18d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 23:01:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 23:01:35 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:01:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:01:35 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 23:01:35 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 23:01:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 23:01:35 GMT
ENV PG_MAJOR=15
# Tue, 16 Jun 2026 23:01:35 GMT
ENV PG_VERSION=15.18
# Tue, 16 Jun 2026 23:01:35 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Tue, 16 Jun 2026 23:01:35 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:04:21 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:04:21 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:04:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:04:21 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:04:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:04:21 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:04:21 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:04:21 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:04:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:04:21 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:04:21 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:04:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2025cc5e12f2cbe6187cd190b9914d33616c8659722105aacfb56031de96df0c`  
		Last Modified: Tue, 16 Jun 2026 23:04:34 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4e6cac7f547d90a803510b19ebf1d4f8703f26d88f9f036a9096f668418b9a`  
		Last Modified: Tue, 16 Jun 2026 23:04:35 GMT  
		Size: 864.6 KB (864633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5542705b1d6a248e18d07d0fb840bbc98f071f2d9c8be1e53559df90c2bfe39e`  
		Last Modified: Tue, 16 Jun 2026 23:04:34 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e471ee7ff8d4ebf804a96ea790c9bc637af5e4078812873220a3a0273ad2b2`  
		Last Modified: Tue, 16 Jun 2026 23:04:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba32e7fc4c2406a45f7f6756446cc925385db85e9a22722ed2746866134bcb17`  
		Last Modified: Tue, 16 Jun 2026 23:04:39 GMT  
		Size: 101.1 MB (101080253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2b508f1ee6478608aff2429979e830b5a52d16d3a1223c73b01522d8d47394`  
		Last Modified: Tue, 16 Jun 2026 23:04:36 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a80f3061a2a266c768d9c4caf5e9544bc9286b4bf37828d821666a949568962`  
		Last Modified: Tue, 16 Jun 2026 23:04:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea60ef47d7c4924efd2eeed332f9a0d744a582380b9559a60ecde79e03c5259e`  
		Last Modified: Tue, 16 Jun 2026 23:04:36 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7dd9c7c2efc3170b6dbcf0966f17a1e8673709589d3b45fd8151a0086f1eb2`  
		Last Modified: Tue, 16 Jun 2026 23:04:37 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7db387a31b84ccd02dbdac3e09fa1e42a5c836b20f5a896b5a093b118bf13d`  
		Last Modified: Tue, 16 Jun 2026 23:04:37 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:178eec6886265c77e3b0ddb94c843c2dc1c602cf22eb18437bdc46b3146590d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.0 KB (641994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2f047bdc49c17d2e1ce3336c67d1acdb587c7a3ce02a71578fe8f731734c6f`

```dockerfile
```

-	Layers:
	-	`sha256:bff7f6a00d809619ef85817be5a6934f85e48f2b16a587655aeb4c2d88e0e5db`  
		Last Modified: Tue, 16 Jun 2026 23:04:35 GMT  
		Size: 597.4 KB (597420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4569f17c490718d421275b201a88a5f25a160dbab7eed27e0b0320628c15403`  
		Last Modified: Tue, 16 Jun 2026 23:04:34 GMT  
		Size: 44.6 KB (44574 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:36d089cd37838927a34708483301d8c227ee7d6cf4b64d96006c1d36ec0ff5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113035946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c7d5f17aebfe32a0d03df4e6431de9ddba582ec745b3bd46e09dcc1f6c08e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:58:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:58:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:58:40 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 22:58:40 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:58:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:58:40 GMT
ENV PG_MAJOR=15
# Tue, 16 Jun 2026 22:58:40 GMT
ENV PG_VERSION=15.18
# Tue, 16 Jun 2026 22:58:40 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Tue, 16 Jun 2026 22:58:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:00:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:00:47 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:00:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:47 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:47 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df74663ebbfa9c3df9a8a67d23e7e06cda4ab31df2cc19fb29fef4f41f03cb8`  
		Last Modified: Tue, 16 Jun 2026 23:01:04 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caf478a86f2daa679a734756555e2755623552114b1c941b042fde5a81f5dad`  
		Last Modified: Tue, 16 Jun 2026 23:01:03 GMT  
		Size: 852.3 KB (852280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638d18704274fbd029b1860006a025ac65f99033e51ebcde6e1237e0b0ee97ad`  
		Last Modified: Tue, 16 Jun 2026 23:01:02 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3dab62a18794e4d29bb2074e4406704f6f2155a47c350a8f7da9daf87de45a`  
		Last Modified: Tue, 16 Jun 2026 23:01:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf8be0f4d1de5e9fb8f89ad329ee6bc3f7272c900fd3604cc9bde6e61839183`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 108.0 MB (107983338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bc3a8776cd2cc9eb1f871388fe933a429960467021039e907717de8a51b5d8`  
		Last Modified: Tue, 16 Jun 2026 23:01:04 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2396c3d3aad325f860d840e5b742cfcad0bce25369a13641a2f0c8b567a2941`  
		Last Modified: Tue, 16 Jun 2026 23:01:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46a3148915045a17bd70096bda9cc9c7a69af8d2045dfc358b68bc331615609`  
		Last Modified: Tue, 16 Jun 2026 23:01:06 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872232136ebaec04ef7a3266b28a84a07ba71c5b88566e47544d2e7e42591607`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ec9c034f182b26d205229243034cee86a679c055cc39a12ee4829ae797cbe3`  
		Last Modified: Tue, 16 Jun 2026 23:01:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:93e79eaaad7de6f6e06ace1eba94c1c4ffaf1f7ad55197fea9cdf21b93e4a099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.1 KB (642054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9244d7c411de1540213a5c30624a054e468b47c4b8fff7cbc20db34b92706238`

```dockerfile
```

-	Layers:
	-	`sha256:b900a76a78b68d5ea8c1da7c2877408c4479792a2c3c54759664b6323584bdf2`  
		Last Modified: Tue, 16 Jun 2026 23:01:03 GMT  
		Size: 597.4 KB (597440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac24c6df65c052ffccef8708d32df3e8352b2a26601eb65a969fa5627661909`  
		Last Modified: Tue, 16 Jun 2026 23:01:03 GMT  
		Size: 44.6 KB (44614 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; 386

```console
$ docker pull postgres@sha256:3e1ec7af92644de059603690d22099b939f98086eb6ffe519f7c57d5ad0e43e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121879556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8751af841d0f9e17cf9ffe1da4fa64e1dc0eaae05d083dc138be5b1a0fe31c4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:58:59 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:59:01 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:59:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:59:01 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 22:59:01 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:59:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:59:01 GMT
ENV PG_MAJOR=15
# Tue, 16 Jun 2026 22:59:01 GMT
ENV PG_VERSION=15.18
# Tue, 16 Jun 2026 22:59:01 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Tue, 16 Jun 2026 22:59:01 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:01:18 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:01:18 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:01:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:01:18 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:01:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:01:18 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:01:19 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:01:19 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:01:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:01:19 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:01:19 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:01:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c7637b3b0ab280eaaa936d8f16a8c0d1cc0ff2c0e0b577663741dff2ebcf05`  
		Last Modified: Tue, 16 Jun 2026 23:01:34 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c31697eeff9774dfc173c92cea2abe434794307ddd141afc125d1cee6081fa1`  
		Last Modified: Tue, 16 Jun 2026 23:01:34 GMT  
		Size: 868.4 KB (868432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93aa24828f6c7855cf554550be7a35ff302758ec6378688a5d07a1852f1372eb`  
		Last Modified: Tue, 16 Jun 2026 23:01:34 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5a57ba19a41a2d6cc7215c141548200b658ade79552a78cf9352d1b803eea`  
		Last Modified: Tue, 16 Jun 2026 23:01:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e69882169991d9431626f4f6dfd80e874c6e980aba8a3b0885e1b6df6c098d4`  
		Last Modified: Tue, 16 Jun 2026 23:01:39 GMT  
		Size: 117.3 MB (117323699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eeb49441b9986d89f9e4683527a90c2480e7859be81cc68f7ecf2495fe510f1`  
		Last Modified: Tue, 16 Jun 2026 23:01:36 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004bac10f5dee9df7a8ab0551ec53adb6b250085a29d19acc79e224e8e82f16f`  
		Last Modified: Tue, 16 Jun 2026 23:01:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1197f535907294952310c4536baeff8deb64438efc7e7508fb897bc3c1305b3c`  
		Last Modified: Tue, 16 Jun 2026 23:01:36 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342aff1984c44d58ae5f1cb1c18a0de0e425c4d525a4a9ab3052a2b629b3cb6c`  
		Last Modified: Tue, 16 Jun 2026 23:01:37 GMT  
		Size: 6.1 KB (6094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1a7c1f0204aa1709df33e8245c09c14d03e2b36586f167f554b921fd28e7f9`  
		Last Modified: Tue, 16 Jun 2026 23:01:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:6898ac1dbf40860cc9b5d070f72d8f6d94d2434df304ffaa8d9814c38ffe3e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbc5ff324ab164f7bcdefa6d140bc15067bfc8af100dc8ebaec00ed7d32a7ee`

```dockerfile
```

-	Layers:
	-	`sha256:08559f9611d5ef5688db35a1600284e3b7eee2160045692079599838c48f81e5`  
		Last Modified: Tue, 16 Jun 2026 23:01:34 GMT  
		Size: 598.0 KB (598009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:453bf5da7c4a71cecad9dc3f9a1be3a23ef514fd57226c2ce1d79b09120637e8`  
		Last Modified: Tue, 16 Jun 2026 23:01:34 GMT  
		Size: 44.3 KB (44342 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:5b1941a494796309edeba10258c46df04183c1343c7de88fb122fee968de1b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117862066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8520d78925050523f132fbb7d3f1ae7ff72161c4cf67d215b742014c988059`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:56:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:56:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:56:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:12:14 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 23:12:14 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 23:12:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 23:12:14 GMT
ENV PG_MAJOR=15
# Tue, 16 Jun 2026 23:12:14 GMT
ENV PG_VERSION=15.18
# Tue, 16 Jun 2026 23:12:14 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Tue, 16 Jun 2026 23:12:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:21:18 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:21:19 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:21:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:21:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:21:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:21:19 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:21:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:21:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:21:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:21:20 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:21:20 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:21:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a550c138b135a89330347b3a13776cce136b1e19d05c3e2b10571ce2135769`  
		Last Modified: Tue, 16 Jun 2026 23:01:22 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86fd92e78cd7b0d10ecc0f0da5decbed7534334b833b91ed30473a9d6fcb1f`  
		Last Modified: Tue, 16 Jun 2026 23:01:22 GMT  
		Size: 857.4 KB (857445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664dfe9e7b8ba874c43b4eae9ed442df98264c6d9336e53b927c836a044de4e0`  
		Last Modified: Tue, 16 Jun 2026 23:17:01 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b334be2a72215ddf0813fb1a98ca70d172379ae40f730d5c2195ba55291ef56b`  
		Last Modified: Tue, 16 Jun 2026 23:17:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b830e10573401f2ea373cdf3504db33d85ee1bee826f7394a3dc5921fcbec46a`  
		Last Modified: Tue, 16 Jun 2026 23:21:56 GMT  
		Size: 113.2 MB (113173930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afda65c3cd9ded55cb2459552d5077f521f9be3d888175390688db8accb6bc38`  
		Last Modified: Tue, 16 Jun 2026 23:21:52 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b1d8c6a5718333105c2454ed4050531e9999b0672ba0eb455f85c76021e582`  
		Last Modified: Tue, 16 Jun 2026 23:21:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f02ae672da66ee4a753bece3dfb28a0dd1de9d30db8e800ab5827840594f72a`  
		Last Modified: Tue, 16 Jun 2026 23:21:53 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b83f789c577c86f82c0d42da2063fc3519c7c3fd37aa97e26ec1e119218502`  
		Last Modified: Tue, 16 Jun 2026 23:21:54 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b731b0ac122661ab6141ccc774e2da27e976618c65913e4a245c608ea02394a`  
		Last Modified: Tue, 16 Jun 2026 23:21:54 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:f339d13ada510f119744b62ca3560484b1538993332854a0560f3eab6dbab542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9ef960a77dbc7410c944157b513d981df1377463dd25c48240ebf98544f710`

```dockerfile
```

-	Layers:
	-	`sha256:b0e80388f0631d6c86c8e04713f90f18009d38600f09290b512cf7bef27da351`  
		Last Modified: Tue, 16 Jun 2026 23:21:53 GMT  
		Size: 595.8 KB (595755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0a6221c913b66dba2f91d2bfef841457802edb355dbce6a5669bd0b4ca1040`  
		Last Modified: Tue, 16 Jun 2026 23:21:52 GMT  
		Size: 44.5 KB (44450 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:9172c561e4fe2caca762a3aab34420e50ff449fae87abfd3e05a74560cde91ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117179650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d14edb3bbb0d9587beab6fda0d143725c70bdec9c26473fe572918548a325b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 05:59:15 GMT
ADD alpine-minirootfs-3.24.1-riscv64.tar.gz / # buildkit
# Tue, 16 Jun 2026 05:59:15 GMT
CMD ["/bin/sh"]
# Wed, 17 Jun 2026 20:22:02 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 17 Jun 2026 20:22:13 GMT
ENV GOSU_VERSION=1.19
# Wed, 17 Jun 2026 20:22:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jun 2026 02:07:29 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 18 Jun 2026 02:07:29 GMT
ENV LANG=en_US.utf8
# Thu, 18 Jun 2026 02:07:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Jun 2026 02:07:29 GMT
ENV PG_MAJOR=15
# Thu, 18 Jun 2026 02:07:29 GMT
ENV PG_VERSION=15.18
# Thu, 18 Jun 2026 02:07:29 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Thu, 18 Jun 2026 02:07:29 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Thu, 18 Jun 2026 04:51:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Jun 2026 04:51:12 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Jun 2026 04:51:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Jun 2026 04:51:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Jun 2026 04:51:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Jun 2026 04:51:13 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Jun 2026 04:51:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 04:51:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Jun 2026 04:51:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 04:51:14 GMT
STOPSIGNAL SIGINT
# Thu, 18 Jun 2026 04:51:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Jun 2026 04:51:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c34e5222b29b86391cdae95b0473ef789493ff1a0068a3a30b5d66f544bd7cf6`  
		Last Modified: Sun, 14 Jun 2026 06:47:00 GMT  
		Size: 3.6 MB (3574358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63bc382ee77772838b6762efb5dc9918aac46cc99c959111411a578a706e8e9`  
		Last Modified: Wed, 17 Jun 2026 21:18:05 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac745ca8a6a40fa8931eea62c6eada5afee35c1c91aede732f42ba0aba848664`  
		Last Modified: Wed, 17 Jun 2026 21:18:05 GMT  
		Size: 844.9 KB (844939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04af9fb0c1657dde4ed06cad73e1f6f1f88358f9c40e7b29d9a9811383c526f0`  
		Last Modified: Thu, 18 Jun 2026 03:02:44 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6162e785d2f8fd62f901324e82906cc4940fd02456304143ec1c4fd9f62f07`  
		Last Modified: Thu, 18 Jun 2026 03:02:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a04deb891798bd66c5d5e5451659706d93ac0b1313f14b1ae67b2c066a91bc`  
		Last Modified: Thu, 18 Jun 2026 04:54:29 GMT  
		Size: 112.7 MB (112743049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8c61136c57792848cb4338d234d316d1ed386df91ba191bd8188b3634f7f12`  
		Last Modified: Thu, 18 Jun 2026 04:54:11 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e326025dd8e2f9842f3f59ccc05f3f11ad55735d7e42f3e68becff1a35116e`  
		Last Modified: Thu, 18 Jun 2026 04:54:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d5992f5ef88b10f7473e79d1d6c74b6007976e2730a15fd582acde68291dbb`  
		Last Modified: Thu, 18 Jun 2026 04:54:11 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331f14155218bfc723eba8719389dca3397d7a17857345d55d8f041d3ec42b14`  
		Last Modified: Thu, 18 Jun 2026 04:54:13 GMT  
		Size: 6.1 KB (6105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e244f207046f419b1c0a01d039983c5fc8e96c299c4f5c5ad53d3b12c22714`  
		Last Modified: Thu, 18 Jun 2026 04:54:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:71791669a4fef945c284bc9c82f37791e5d9b3f5183fde14f1d1a6fa1cdcbf1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.9 KB (641863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413bb4645ee480bd9c901cfb65e2beb8a78ae349b60bca15104b5901fee9454f`

```dockerfile
```

-	Layers:
	-	`sha256:d0fd7e3a0cb128f48aa01e6af1e7f57a78300dcef742580286d70667c4bd8789`  
		Last Modified: Thu, 18 Jun 2026 04:54:11 GMT  
		Size: 597.4 KB (597413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24d7742525ae91af6ab0aef2de481d9410542cdffc88ccc5ff5a9ee51d8a560f`  
		Last Modified: Thu, 18 Jun 2026 04:54:11 GMT  
		Size: 44.5 KB (44450 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:8aefb98f4419e46c0b23701abd3b3123166f5468e9379f9178d3aa3d19d2dbc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121694340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131e7e60bf6e5c0c7901e1e5c8ce047ed10c6a4890defa401ade0e2a671e01bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:56:31 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:56:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:56:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:02:05 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 16 Jun 2026 23:02:05 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 23:02:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 23:02:05 GMT
ENV PG_MAJOR=15
# Tue, 16 Jun 2026 23:02:05 GMT
ENV PG_VERSION=15.18
# Tue, 16 Jun 2026 23:02:05 GMT
ENV PG_SHA256=11df0df97fe3ea4ba9a791faaf39cee1d2fe571e78885b5b55d8517d27c323b4
# Tue, 16 Jun 2026 23:02:05 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:11:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:11:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:11:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:11:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:11:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:11:33 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:11:33 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:11:33 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:11:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:11:33 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:11:33 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:11:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52132c4d8fde8082c15540b29256e2360f2c6de68191ad0e46bc71ec74cdc17f`  
		Last Modified: Tue, 16 Jun 2026 23:01:43 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abc6a5451d4cc8391999b7fe99a4a79df7ab9b3d307f2f9e012ae4ea28dfb70`  
		Last Modified: Tue, 16 Jun 2026 23:01:43 GMT  
		Size: 874.5 KB (874490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0731dcf5cb2d8b3c5ed62f929b7b76fb4b1869f59ae839f8acbc53f3d0ca44`  
		Last Modified: Tue, 16 Jun 2026 23:06:56 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c5dd37845c73dafd37443171cc6c2df467255dc46daa591bd1c37afbb9b189`  
		Last Modified: Tue, 16 Jun 2026 23:06:56 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2d7da1333e42eb58258d7aca7555322a0a1acdb98e4e02e18b2b39419daaa9`  
		Last Modified: Tue, 16 Jun 2026 23:12:00 GMT  
		Size: 117.1 MB (117093248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3932e7352ec01c96ac23d711f362746e49a93adde04878701f40802a99cc239d`  
		Last Modified: Tue, 16 Jun 2026 23:11:57 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2d20b2638c026a15d9b7029f15c3b1f0fb18898b2d93f91c68a869e86cd4b3`  
		Last Modified: Tue, 16 Jun 2026 23:11:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7073ca6e6bbd42d855a0e1e7ac66d57f758c1b6fc0c9a18fbf9bf26c9acf7d72`  
		Last Modified: Tue, 16 Jun 2026 23:11:57 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cfa0cc18b00d6d759c663db3c404dd10f1f59d3305a6fdce21ca7923790375`  
		Last Modified: Tue, 16 Jun 2026 23:11:58 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcbe2ab3014ba52df871bdb42059206e28d2dbc697e36f20aca3fdeebe4bb6f`  
		Last Modified: Tue, 16 Jun 2026 23:11:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:0e4b11c41955d3a0f8f5e35e127a3aad887c436c22ed2c40d3451074115377e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.8 KB (641773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ada34c7b1459926b5e6d7e044904379f72b35d3c94620a21bc8425fee994dc6`

```dockerfile
```

-	Layers:
	-	`sha256:6471920d33c09c571026d635fcdc9efe01124031be58f07129a3dc25a47f7613`  
		Last Modified: Tue, 16 Jun 2026 23:11:57 GMT  
		Size: 597.4 KB (597383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e06b44ebc465b2398b5f442c7c94aade166962e1ada26ec0c5cea3dfee5c05b9`  
		Last Modified: Tue, 16 Jun 2026 23:11:57 GMT  
		Size: 44.4 KB (44390 bytes)  
		MIME: application/vnd.in-toto+json
