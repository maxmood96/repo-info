## `postgres:17-alpine`

```console
$ docker pull postgres@sha256:d93aaac29e4e7525c29b6f6b9ec982a0950c1ab408f6fa9af67705c651f0a8c4
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

### `postgres:17-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:e81e6e8ca50f8c08f2d6d0e434e7b40238434107e2ed51f8282210305d9326cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113071635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102661e174e6ad678d4f99a2bfde8c0ec138acda93cc89e4adf26090aa45d1bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV LANG=en_US.utf8
# Mon, 08 Sep 2025 20:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_MAJOR=17
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_VERSION=17.6
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Mon, 08 Sep 2025 20:04:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 08 Sep 2025 20:04:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 20:04:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Sep 2025 20:04:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b431e71196b5718e79135ea72965b9f308ee9739aa6eefe7f2a30329a2381f`  
		Last Modified: Mon, 08 Sep 2025 22:42:17 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0ade3a132d78770b9f55c4064042c3bc248e632172bafaa855966379ae5f2f`  
		Last Modified: Mon, 08 Sep 2025 22:42:17 GMT  
		Size: 914.8 KB (914824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cd10be37f4046fe8150370571b316af5bdeffabc96015c344a2632e427ed13`  
		Last Modified: Mon, 08 Sep 2025 22:42:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb0f042d918067fc21b8294420d0af826759481e62f31f3d0b38f70611b229b`  
		Last Modified: Mon, 08 Sep 2025 23:12:27 GMT  
		Size: 108.3 MB (108339744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a58bb42c06918a33c71bebc61048641c8675894660f0f1c67c7c1e3e0d262d`  
		Last Modified: Mon, 08 Sep 2025 22:42:16 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76416bd8113e1e4cfc8aec32acfb244bd299d4879c379c1cb0cad63117789a37`  
		Last Modified: Mon, 08 Sep 2025 22:42:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8914ca6edcdf53fdb2ff5d0a37068ba0f165f1064225bed1896bd00998370163`  
		Last Modified: Mon, 08 Sep 2025 22:42:18 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a693e6a145c7a9b2d9f713e31bfe0b0b049eede8bb524418fc02ad1ad8f97751`  
		Last Modified: Mon, 08 Sep 2025 22:42:22 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f8ead99dae4f8fc42014c427f9ec05676f135e4cca864c67cf12732eca9d5b`  
		Last Modified: Mon, 08 Sep 2025 22:42:17 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:6ae46c86fba72a7cbba6ad33fc0bcce9077ab42b3a37c943b028006f3f8f36ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.8 KB (639808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dab9bdc9ab3a9db4fd8c1365aee3fa40d40beeea486b83848b5a45e18eb873`

```dockerfile
```

-	Layers:
	-	`sha256:c8726e6274a159aeaa202d62d85b943b5c45bee5cf070fdaea82e533861540b2`  
		Last Modified: Mon, 08 Sep 2025 23:12:25 GMT  
		Size: 597.5 KB (597543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14cd8268ec38ca3b8f0b40f933a5b8c9101240f82632313eac5b775156c4e172`  
		Last Modified: Mon, 08 Sep 2025 23:12:26 GMT  
		Size: 42.3 KB (42265 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:6db6bb70847a7b85516273f1b5954e6d43527a0eb0cda5df5e40faa121a8655f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90313234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d5cce094f747a37eae97eb18fbb850bbea21fa050ba76ee23a85e8bc004405`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_MAJOR=17
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_VERSION=17.6
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Thu, 14 Aug 2025 17:12:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 17:12:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:12:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:12:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079a1c87b1e4afd06564bb4788685a8121d0bc8ee1c65f7d29bae031097a898c`  
		Last Modified: Tue, 15 Jul 2025 21:59:03 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e018b614d5cbf1a0d8a1b23f428d5cbbbe192798ac0751d81172993ca1dbc93`  
		Last Modified: Tue, 15 Jul 2025 21:59:05 GMT  
		Size: 1.1 MB (1083508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aebdb48dce72469d3bc8e6f100e27f0b1c674d0a7c8519656f5c74d79da67ac`  
		Last Modified: Tue, 15 Jul 2025 21:59:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a2127a753a0aa1d58a9ac13d37a4c900af90f5d538d854be365215ab7a81a3`  
		Last Modified: Thu, 14 Aug 2025 18:30:50 GMT  
		Size: 85.7 MB (85711438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e776cf980b94cc3d79adbb32c0cc125b80b4004d64e5d0e25220e40ec9c199`  
		Last Modified: Thu, 14 Aug 2025 18:30:32 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b165d0bf72080f70e9773ff7256985fbf1396ef354bb4371b800467c6ef4983`  
		Last Modified: Thu, 14 Aug 2025 18:30:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2499ed557a6de5314add32b6c0742c4ab947038908358af0f8c49365df800d`  
		Last Modified: Thu, 14 Aug 2025 18:30:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a12802d00441b5c8b5a352df41e579b5965b6d4b36c908bfdb22aa16d759da6`  
		Last Modified: Thu, 14 Aug 2025 18:30:33 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0daa41fd528c8dea6a642aa4545831cc69ead2e188b23bb48c7d8b7479b598`  
		Last Modified: Thu, 14 Aug 2025 18:30:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:034fefe0998c6a9ba82bef12150d8fd2a78d2dee6db328233da22da91e765ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 KB (42235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e4140fd59d8453f48f7beae838559c1e550f3c61ec6913b9d62222752965ed`

```dockerfile
```

-	Layers:
	-	`sha256:cd265b7275eccbbd45b2a7cb0f5def63c8dc8cf6dc6793a4b14e869b47e19dce`  
		Last Modified: Thu, 14 Aug 2025 20:16:49 GMT  
		Size: 42.2 KB (42235 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:3f7f2949ce9fde882e2f139e396ee42c9d7b2b82ae4e1fe790ea7c8cb3f7d82e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85551881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ef2ed4feec6e83cc9099102866d1bdfc01ac6c881955356e08343168db2266`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_MAJOR=17
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_VERSION=17.6
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Thu, 14 Aug 2025 17:12:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 17:12:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:12:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:12:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d311585bee083aa9525f093872b6272f30fd05678140622cf8b253423af3dd`  
		Last Modified: Thu, 14 Aug 2025 18:50:36 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36a7751694a53e9a57d5356c38e15bbc8420fe128dc24f6b1156e5d65657148`  
		Last Modified: Thu, 14 Aug 2025 18:50:36 GMT  
		Size: 1.1 MB (1083514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316e9eecd02a521a3ae56f56f8c8424e494df30dcbb73367d000ee2612ca7ce3`  
		Last Modified: Thu, 14 Aug 2025 18:50:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56e93e5e348f589605c4583aa0ef68ff1e619192a64e34e266527bcb68c932e`  
		Last Modified: Thu, 14 Aug 2025 19:32:13 GMT  
		Size: 81.2 MB (81231950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a9c576300f4c36337bd343bdc718aafd0ae47a8678b4e25936cc169e0edbf2`  
		Last Modified: Thu, 14 Aug 2025 19:32:05 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9261a27b22948ab76831061d3eaf06f02960d3284b3b1ff04fe16632df9591a3`  
		Last Modified: Thu, 14 Aug 2025 19:32:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0cb5a4c1c02a5e194b22c4708d0d6fc5b137e1f38ae855315909ac3dfb3d4a`  
		Last Modified: Thu, 14 Aug 2025 19:32:05 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583b3fb2676d19bd324d217455eee96657addcc11a4b56ff673a7cc4b657a58e`  
		Last Modified: Thu, 14 Aug 2025 19:32:05 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac8085058c41318810af66d09a0789371e5fca639b5d89124c6eed7257edafb`  
		Last Modified: Thu, 14 Aug 2025 19:32:05 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:ba44e33c01abbdb7aec5e9dd4701fc815e4bb28bba1365012111a5ab9e466383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (640049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9da36c6f0d91793267a4309cb6dd58fd77eeae16344e3672f9fbd46c6348d42`

```dockerfile
```

-	Layers:
	-	`sha256:f4679f8c353b4f10e991c353c771376f19b1603243c32b6c2866f8654188571d`  
		Last Modified: Thu, 14 Aug 2025 20:16:53 GMT  
		Size: 597.6 KB (597599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b133b19a7e78f696b6227f836e584a3fa3fcc7a5a1a3456e6eb930af30fe08c5`  
		Last Modified: Thu, 14 Aug 2025 20:16:54 GMT  
		Size: 42.5 KB (42450 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:6d76cef88ff8e5995066a8878fb16b7d613fbaccdf695e57e85eaadd74e663d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106721846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e21f75150d1710b4ed04202d22322d11ae667dcb448fbb87f9549d9f2df00e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_MAJOR=17
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_VERSION=17.6
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Thu, 14 Aug 2025 17:12:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 17:12:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:12:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:12:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5c482840cf82de196008abc359484735770b13c9282408f1dca4d75164f7d5`  
		Last Modified: Thu, 14 Aug 2025 18:54:31 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e157a09d862e13d8d0e716ab97e9d5a2c94438123a639c16e3eab984125883e`  
		Last Modified: Thu, 14 Aug 2025 18:54:32 GMT  
		Size: 1.0 MB (1042499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e8baf5ceef7de553a728a2b722a0c9dd8f8640b8e0595991a87034be1cd7c9`  
		Last Modified: Thu, 14 Aug 2025 18:54:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e4a7959416027147044e7c53337a20ff8f69b09651cd85c477e159c314ab7b`  
		Last Modified: Thu, 14 Aug 2025 20:16:47 GMT  
		Size: 101.5 MB (101531219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ee027c6f2dd72f7bc24add06070d2c058ef1e58c890481c79ed793137b5868`  
		Last Modified: Thu, 14 Aug 2025 19:14:34 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8d261c1de621bda61e327a3a8dc8f628cd64d3c1d1b9c1c1cc9be3f0b1a64a`  
		Last Modified: Thu, 14 Aug 2025 19:14:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4be87c09082a970c99b1ccadbe7619b5eb9932e5f6069ab57a5fe544ea596`  
		Last Modified: Thu, 14 Aug 2025 19:14:43 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e2821a53299d452ec3d59cc79f64eb8aa88f32b18c7f766b07f642f7d10532`  
		Last Modified: Thu, 14 Aug 2025 19:14:46 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc7181549e9bfc56dd22e511ef32b30445db856e4d8398064242caa38bdcf2b`  
		Last Modified: Thu, 14 Aug 2025 19:14:49 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:924b42e61a9c95001ae81873c622e92cad5f85056a1394dfe46c8cbfff29281d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.1 KB (640133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375806b3995a6a54bec3ad4e189a94ba08cd6128b0a4ce94e4d641185db31b7e`

```dockerfile
```

-	Layers:
	-	`sha256:31a2aaa214d375b8745518b568fea6e8433c87d0db25b580d64532488e0182d3`  
		Last Modified: Thu, 14 Aug 2025 20:16:58 GMT  
		Size: 597.6 KB (597627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0f69a1126b00f05162d493f5336043aaa645006393505591fb94dc974a4c74b`  
		Last Modified: Thu, 14 Aug 2025 20:16:59 GMT  
		Size: 42.5 KB (42506 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; 386

```console
$ docker pull postgres@sha256:cf0bbe88a71100c6af722bfb0536282ce9b80faef73240606163d7ab0af94325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119143861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3e4ac56be73e3b5090b1b1864ad1d53dc830a273d8fa1b0fc8e0ece4851f68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV LANG=en_US.utf8
# Mon, 08 Sep 2025 20:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_MAJOR=17
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_VERSION=17.6
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Mon, 08 Sep 2025 20:04:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 08 Sep 2025 20:04:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 20:04:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Sep 2025 20:04:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81c2502f20ecb5ecc4f24c8463f3c291d2f5dd801b98ff61756e2b787ad3f21`  
		Last Modified: Mon, 08 Sep 2025 23:13:49 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2953fd291b77bf85ee2b51b51c621ff1be5ca81d0075b3615d57d5fc379195a`  
		Last Modified: Mon, 08 Sep 2025 23:13:52 GMT  
		Size: 885.2 KB (885200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a016184891a225ab007955b7ab9783f0e6e1e7561c389ac88a8b1db29c9ceacd`  
		Last Modified: Mon, 08 Sep 2025 22:41:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60607e2fd467e7efe3300b7ff69e1f908ab285debbfa2d5f7193cbdee9ba5a42`  
		Last Modified: Mon, 08 Sep 2025 23:13:55 GMT  
		Size: 114.6 MB (114626283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7d150ea08beaf10ff364938812d234cc7f2cdf6425cbf1c5c7230eaa556dc4`  
		Last Modified: Mon, 08 Sep 2025 23:13:50 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b54a7e53aa43a5d57437d113097cb67423ae1a3db3ad3b7e7b94c83f692637b`  
		Last Modified: Mon, 08 Sep 2025 23:13:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f24b59565249812de9dc881eebdff1aefa2654e56841a5e61956ae58f2b96c0`  
		Last Modified: Mon, 08 Sep 2025 23:13:48 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837aa8ae2d0499c48d7301d9af37a6779db1e6cc8fc0ad71318a3aa7f0d9b658`  
		Last Modified: Mon, 08 Sep 2025 23:13:51 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5c3e2c42ea6c9a5106b888b4b9d98460fc26ca0700fde89729c6d1a3731112`  
		Last Modified: Mon, 08 Sep 2025 23:13:47 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:d8353adf1c2de5c966907facfb015a3a24aad1174a1db1c64685dc7ccfd764e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.7 KB (639716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d3d20240f0280e4082d38f184a9722b683101dfb04e5778b1179a38b850008`

```dockerfile
```

-	Layers:
	-	`sha256:9557417f093f2c8c5cac4c3cdb3cd67513c98f03f710c451f4de588a9cfc41a9`  
		Last Modified: Mon, 08 Sep 2025 23:12:36 GMT  
		Size: 597.5 KB (597508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa3d94b4718530d62241153f6f11986358d7c0f046bd8e349182b42dba86d23b`  
		Last Modified: Mon, 08 Sep 2025 23:12:37 GMT  
		Size: 42.2 KB (42208 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:ce684d3c33fe026e71e23d8d0637caf7685845c2f51662b70bdd871cffae6f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94586981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328f2e9c931735e9577d43ca83aab167440caef73209b563b8f03791b91fbd6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_MAJOR=17
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_VERSION=17.6
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Thu, 14 Aug 2025 17:12:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 17:12:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:12:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:12:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5ee779caf31f6000861b5a827cc767777a7e523406271d594906edba47fb17`  
		Last Modified: Thu, 14 Aug 2025 19:04:33 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39e84474c9e8b921b5d1f181c420c8539aaff375b40eaaf2fb3eaa645a3f1c3`  
		Last Modified: Thu, 14 Aug 2025 19:04:34 GMT  
		Size: 1.0 MB (1032220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e3db6901ab70acd1d995ed99e8573dea313f7a01c50aaf9406525d32cee2f7`  
		Last Modified: Thu, 14 Aug 2025 19:04:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dfdee8889aee12a03bd5a775c795250213fb0741de60e74d596c10f7b88097`  
		Last Modified: Thu, 14 Aug 2025 19:16:51 GMT  
		Size: 89.8 MB (89810254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfa3d797f9a589fccc2cc197e98ce781c79552da3784827db02b45ff279bdf4`  
		Last Modified: Thu, 14 Aug 2025 19:16:41 GMT  
		Size: 9.9 KB (9892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcfe4688567daff39132560ea37a709781c386871ef7666b18a5d31f8edf9b2`  
		Last Modified: Thu, 14 Aug 2025 19:16:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401b65c5316bb49caa4decf6179d1ea8141e87f6311711835ab7e974ffbf5d38`  
		Last Modified: Thu, 14 Aug 2025 19:16:41 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e795f7a5d2fa0c9f1cd36186829513caf4e5f652ed2445a2820fe4b04b421a48`  
		Last Modified: Thu, 14 Aug 2025 19:16:42 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f04887b1d22d3f778ca6b8e609f81cf7d170394001426051fd261ab028bfd6`  
		Last Modified: Thu, 14 Aug 2025 19:16:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:bbaf9f326f3776a2e2a7fef5a50e90c73a233bbebd7e71e6ac08b8dafcecd555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.3 KB (636317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9bdc19a9a1309aad0673865608bc2422e471f94182b53345bab98d000b51b4`

```dockerfile
```

-	Layers:
	-	`sha256:359f3cf9186110b1f54cd03365154a012f1243c438e6cae3312f87177c55cbac`  
		Last Modified: Thu, 14 Aug 2025 20:17:07 GMT  
		Size: 594.0 KB (593980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91cc1b5729d6187b36764076503169fc5256a4214c2eb3bf8064eb8c9169f8d9`  
		Last Modified: Thu, 14 Aug 2025 20:17:08 GMT  
		Size: 42.3 KB (42337 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:1403d8f16c5c7c96b3f5e2e11cbec1c19a5ec31021b88bfbf2dd3ba43e529a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110893229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32660e0a115a544c296d19e323d9938b5bfb221855636a6f32007633aea6694f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_MAJOR=17
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_VERSION=17.6
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Thu, 14 Aug 2025 17:12:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 17:12:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:12:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:12:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e4bf5c01f5fd5d5c2b6c78d1d884c92b6fce072812c2b64d8f250b5d9d572a`  
		Last Modified: Thu, 17 Jul 2025 04:54:24 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac990c2f318af1f8860277d49db61df409ca94944240be61871dfc66778de791`  
		Last Modified: Thu, 17 Jul 2025 04:54:24 GMT  
		Size: 1.1 MB (1085426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fe88d6b8c1e7636cb895a96fba5a432b018f4777143e5c57571ff4e73f3ce5`  
		Last Modified: Thu, 17 Jul 2025 04:54:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b983c96cc38fa9714c507ebec42340110b2bccc74bc0abbc4894e74a737579`  
		Last Modified: Sat, 16 Aug 2025 13:24:45 GMT  
		Size: 106.3 MB (106277617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be014f7e7c137809ed0cb37d8e671f03304c075a8d6735fd0816f101040ea07`  
		Last Modified: Sat, 16 Aug 2025 13:24:33 GMT  
		Size: 9.9 KB (9889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf176c153617be4b0a64edd11b0d12ccf129d1dcee2a9146503d90aa01f97ee`  
		Last Modified: Sat, 16 Aug 2025 13:24:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d87fcd22e9ce3b04ff6b04416c5d137bfc27d685e5eb863529ee898abc8105d`  
		Last Modified: Sat, 16 Aug 2025 13:24:34 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a6df0bff6f22a543f44ff88d975a3056018f6254f5163f95ac95ecb1f295a8`  
		Last Modified: Sat, 16 Aug 2025 13:24:34 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8733618b1c54091b0000e6472a8ea04a0c6bbe755b6c2226c179931079177a`  
		Last Modified: Sat, 16 Aug 2025 13:24:34 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:b2a5ac727c5fe1037e5e318ea96dc05b6d62abb764ff5bf17c01573735266641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.0 KB (637981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c6a99b67e1fae48a323e4fe81d403d9f9779cdf87b5a320258ab14b5cbe261`

```dockerfile
```

-	Layers:
	-	`sha256:5093594ceebdc4f1cb0c52ead037c3ad36ed3512aa0e9aec827d657dce487dad`  
		Last Modified: Sat, 16 Aug 2025 14:08:48 GMT  
		Size: 595.6 KB (595638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26acf13b2a939cf3940b37371c0c75dd804654a2911ac82474a81b36bd30fdaa`  
		Last Modified: Sat, 16 Aug 2025 14:08:48 GMT  
		Size: 42.3 KB (42343 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:8b99af6247dac23866fd8d0832074afb9179447304de36c8be3d1eca7c9b2a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119473941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ee7419b809450423e092ce54f2ed54f5575ae740995f6bdca43497ed52dfd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_MAJOR=17
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_VERSION=17.6
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Thu, 14 Aug 2025 17:12:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 17:12:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:12:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:12:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d38346a6df0fbebdd4778252bbd39ccc90b12f4fad75fe53f1e3c72e66c3a5`  
		Last Modified: Thu, 14 Aug 2025 19:23:02 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0825e8e3a340fc788e6927d6d834d1119ad7c294a2a2b22dae232cf44b292106`  
		Last Modified: Thu, 14 Aug 2025 19:23:03 GMT  
		Size: 1.1 MB (1081138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea3f727da024f1366d4f6c638daee81eb74edc322397336acd9044d9a59407e`  
		Last Modified: Thu, 14 Aug 2025 19:23:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b7891df61f410c3838f49153904e837a072a245f29f926f9bcf5ab74e16aeb`  
		Last Modified: Fri, 15 Aug 2025 01:45:10 GMT  
		Size: 114.7 MB (114730447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cbb4e5fc58e7a1daa3fcd9f6eda99fa3528ac711b958bb67217b140dd308d2`  
		Last Modified: Fri, 15 Aug 2025 01:45:00 GMT  
		Size: 9.9 KB (9889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6277582c614e9e1724108dfdcf640f7999f12ef5d5d8341a188fa8880f6adf`  
		Last Modified: Fri, 15 Aug 2025 01:45:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5934507af77e0c3730a53a7325c3c9db3f3a5917d0412bb7b6c22c5317a7c46`  
		Last Modified: Fri, 15 Aug 2025 01:45:01 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ab4e9524963f9c51a1295c4180683106404c5fa7dd33db3bc583f7bbbb6d52`  
		Last Modified: Fri, 15 Aug 2025 01:45:01 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae147157db1fd965c79b23738689b768c2167146ba4500940ef4c1039161d151`  
		Last Modified: Fri, 15 Aug 2025 01:45:00 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:75fde83cfe3daa4044db8a26164646444e260b65dbeab197452dc0f752e8c0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.9 KB (637868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2006a06c562b96872b299c9c104676f107d5fb7bb58a232a7d66bd032530013b`

```dockerfile
```

-	Layers:
	-	`sha256:92e144bcf95da70a1b4e648b9116d7c0aac528ff66a141896c58538b481dd1cf`  
		Last Modified: Fri, 15 Aug 2025 02:09:20 GMT  
		Size: 595.6 KB (595596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0722a1983ef73516cc4e725aca2be6d195a35be4e740847585dde684cefca2a`  
		Last Modified: Fri, 15 Aug 2025 02:09:21 GMT  
		Size: 42.3 KB (42272 bytes)  
		MIME: application/vnd.in-toto+json
