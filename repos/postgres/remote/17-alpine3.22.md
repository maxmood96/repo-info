## `postgres:17-alpine3.22`

```console
$ docker pull postgres@sha256:b02d9b5bcf608c2719da32cdabee274a33841202487fd5dc9b065b63f886753f
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

### `postgres:17-alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:3c9fe01c436ddf61b7803781f677165d2eb0b5f16e1ff9b71787b25d596952f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110689273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0974cb4dd3b8bd23b4529aa5d4f5b5cf6fccb56dbde8e4c70123d505a71783d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 19:01:33 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 19:01:36 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 19:01:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:01:36 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:01:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:01:36 GMT
ENV PG_MAJOR=17
# Thu, 14 May 2026 19:01:36 GMT
ENV PG_VERSION=17.10
# Thu, 14 May 2026 19:01:36 GMT
ENV PG_SHA256=078a03516dcdbdb705fecaf415ea3d13a956c589e46f09fed68a06fb00598c90
# Thu, 14 May 2026 19:01:36 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:03:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:03:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:03:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:03:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:03:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:03:55 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:03:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:03:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:03:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:03:55 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:03:55 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:03:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fac79663628b2ce5eb67069055dee04c957b0181637ffd510629fba63aa89c`  
		Last Modified: Thu, 14 May 2026 19:04:11 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f542ca77777b8504f4a992d39ddbe67bb7a8091a2f96488dff6600d374c0a25`  
		Last Modified: Thu, 14 May 2026 19:04:11 GMT  
		Size: 917.4 KB (917423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2241a1404990615cbe02cfac8e23f4d9808ce390956201e078ec21f5c7982de`  
		Last Modified: Thu, 14 May 2026 19:04:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd53c771c75c6864404012b6ff822235ab7810efdbb3014707f80a428ccad080`  
		Last Modified: Thu, 14 May 2026 19:04:14 GMT  
		Size: 105.9 MB (105946032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821b5a60dbcc46a04923645bc8bacdb6424440165c70402503c907755c3236ca`  
		Last Modified: Thu, 14 May 2026 19:04:13 GMT  
		Size: 10.0 KB (9958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7515b9e4e08503dd00e53082ef3fe4610ebb4a1f81a8b06158e97f5c28ad9a39`  
		Last Modified: Thu, 14 May 2026 19:04:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ac709d94dd1413a2107c1b0012d7340d9e04545721fb02258c7795eea3f29`  
		Last Modified: Thu, 14 May 2026 19:04:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33341e81d564255da0a43bf8db9075b101480c10228ee7c7147b74b4d3691ef`  
		Last Modified: Thu, 14 May 2026 19:04:14 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db2a369ff51c3808f70cde775284e305a5c60dec8d2180ab892c26544726c29`  
		Last Modified: Thu, 14 May 2026 19:04:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:d493f32da01b3783da82b805b51227586c3bcb774bbc27a3698f6fc0f5733bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.4 KB (637378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2fa1c644fb4f0ce0299e712e472972713664e870e28bba486aa6027689c8f5a`

```dockerfile
```

-	Layers:
	-	`sha256:fc7545405b248b704be77d7d962ea01472ea1014d41bdb02f47887318e6852ee`  
		Last Modified: Thu, 14 May 2026 19:04:11 GMT  
		Size: 596.3 KB (596315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22ee59c43275519e3f439de19b4fd63c1564fcf88f5771075e760aeaadda4ff1`  
		Last Modified: Thu, 14 May 2026 19:04:11 GMT  
		Size: 41.1 KB (41063 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:e2f729f4554216a50df65dd98e6f5a1f1ac162c8489d9c26df2b95b083887a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90202174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf8599a2f66664a742b52b67919c31a5f7fc0838d52ab26c15565129c21cad9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 19:17:27 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 19:17:30 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 19:17:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:17:30 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:17:31 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:17:31 GMT
ENV PG_MAJOR=17
# Thu, 14 May 2026 19:17:31 GMT
ENV PG_VERSION=17.10
# Thu, 14 May 2026 19:17:31 GMT
ENV PG_SHA256=078a03516dcdbdb705fecaf415ea3d13a956c589e46f09fed68a06fb00598c90
# Thu, 14 May 2026 19:17:31 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:20:36 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:20:36 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:20:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:20:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:20:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:20:36 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:20:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:20:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:20:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:20:36 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:20:36 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:20:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5b8e72d42e67bad9a63317238d8004d0bf7e3e7da909bdc91f7d999a4ed572`  
		Last Modified: Thu, 14 May 2026 19:20:46 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562c9178a70fa39ec60ac1093144f0fddbb46c78f2f312d514ae26111da59115`  
		Last Modified: Thu, 14 May 2026 19:20:46 GMT  
		Size: 885.1 KB (885147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2473956ffd8839b4b3a0cd3a905e7e441ee23bb2d0e198e7c9c25f5c12ac36e0`  
		Last Modified: Thu, 14 May 2026 19:20:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56419d15f30c15e910bc04f7add2eba5c725ebaa0c11dd25b2dfe5d41c0ea1c`  
		Last Modified: Thu, 14 May 2026 19:20:48 GMT  
		Size: 85.8 MB (85792019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16956085fef7b1390690b282ca54fd4fd63d43c26b6765d2d5676955fd6786e`  
		Last Modified: Thu, 14 May 2026 19:20:47 GMT  
		Size: 10.0 KB (9952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7944fa9f21a5630b8b6553afd415d489500069c273465587dc8a5a0a28e179a`  
		Last Modified: Thu, 14 May 2026 19:20:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb767816391477250bbb58a4726611704a42716875464b541dcbb5c6db1c9a5`  
		Last Modified: Thu, 14 May 2026 19:20:47 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdfa1d0fe79b52f50588383a0f0d129a853b83922f4d6d5c42c0b1795d7b2fd`  
		Last Modified: Thu, 14 May 2026 19:20:48 GMT  
		Size: 6.1 KB (6102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14616ce9354cbd83eb4288b2157d971beca56c0446fcb9ccc573ba6660efcc5`  
		Last Modified: Thu, 14 May 2026 19:20:49 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:bea6fc3c8f16c06b6d4f8721b9499c129485d6fc8e425f569e5b7bcc81119893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 KB (40999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c899ed7c461c9a55ab6eaa9fb120c56f15479c4f1866f82fb95fae83ace6784a`

```dockerfile
```

-	Layers:
	-	`sha256:cf9e9aae13974fd60f142b41b4685324ec26c4c2056d194ef2b53eba3551ed84`  
		Last Modified: Thu, 14 May 2026 19:20:46 GMT  
		Size: 41.0 KB (40999 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:4708f7ea042bb5250dbed3daff0bdef4dc48c9910cd94da54b6cda60ec45480e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85431170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd8b8e8c58c36349e66dd72126640eae44c19ffc3207034d97d8729bb611f43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 19:13:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 19:13:59 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 19:13:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:13:59 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:13:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:13:59 GMT
ENV PG_MAJOR=17
# Thu, 14 May 2026 19:13:59 GMT
ENV PG_VERSION=17.10
# Thu, 14 May 2026 19:13:59 GMT
ENV PG_SHA256=078a03516dcdbdb705fecaf415ea3d13a956c589e46f09fed68a06fb00598c90
# Thu, 14 May 2026 19:13:59 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:17:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:17:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:17:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:17:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:17:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:17:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:17:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:17:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:17:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:17:01 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:17:01 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:17:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436adcb648535e7b4f93081a893d770b80fbc6860c71e2047c1d10568ee0c001`  
		Last Modified: Thu, 14 May 2026 19:17:13 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b644a51e1ad026790deb11ec3668370c104bd9c84d6ffc61307821f83bf9f28`  
		Last Modified: Thu, 14 May 2026 19:17:13 GMT  
		Size: 885.1 KB (885150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c6670df5747768873a031c44935102aa029779640cd943eaadbb5135627ec1`  
		Last Modified: Thu, 14 May 2026 19:17:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9218ce42628e2f639350aada2c6682aa00c6c3e37949bad14a8f30115bef3d23`  
		Last Modified: Thu, 14 May 2026 19:17:16 GMT  
		Size: 81.3 MB (81302570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19fcfc5eacadaf6ed8cec05f9c3f2f7e7df23ee4a76709fd92d3fa5df6336d`  
		Last Modified: Thu, 14 May 2026 19:17:14 GMT  
		Size: 10.0 KB (9953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9984de8642bb9e06b3d107a3439bdeb4ab8c9c1910320377c161c6248a57b3c`  
		Last Modified: Thu, 14 May 2026 19:17:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69755297db7afe467b09cc941e1f340da518c320b6efd2438a2aa6eacccced5f`  
		Last Modified: Thu, 14 May 2026 19:17:14 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8887761faf2f37d5d4c63e9636656fbd3b2ae3e2e569c2534a90618db9b757`  
		Last Modified: Thu, 14 May 2026 19:17:15 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd445decca66067c72de220718d455265e224cbe56dbeaf5f8a69b464e55808`  
		Last Modified: Thu, 14 May 2026 19:17:16 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:739ac756bc6cc8853c2c7f63822dc53b8bd8b78252f419907f1c144824050c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.5 KB (637549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ab8a199d53dc692ef9816d16143d0575b5248ffa7c7644d63e4fae374e49b7`

```dockerfile
```

-	Layers:
	-	`sha256:a35183e464c6964fc2ebf86e6014e3de3f1c8a496f1916929b69c0e4a2092d34`  
		Last Modified: Thu, 14 May 2026 19:17:13 GMT  
		Size: 596.3 KB (596335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b93c8176b47eb9908e6e06e825116221f5cfa10e4d04471a35a04fbbda1de3ae`  
		Last Modified: Thu, 14 May 2026 19:17:13 GMT  
		Size: 41.2 KB (41214 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:7203d89f32bef13d06deb7b43e811357c0be0e2178fd4bb9f070960f4d5a6f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106653582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb058accef8f7483c7b31d8f12da16701931d83ae6d21d5762ba64bb537a63a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 18:58:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 18:58:35 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 18:58:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 18:58:35 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 18:58:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 18:58:35 GMT
ENV PG_MAJOR=17
# Thu, 14 May 2026 18:58:35 GMT
ENV PG_VERSION=17.10
# Thu, 14 May 2026 18:58:35 GMT
ENV PG_SHA256=078a03516dcdbdb705fecaf415ea3d13a956c589e46f09fed68a06fb00598c90
# Thu, 14 May 2026 18:58:35 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:01:19 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:01:19 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:01:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:01:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:01:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:01:19 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:01:19 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:01:19 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:01:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:01:19 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:01:19 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:01:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8533b3f3a288f3b34cef9ab0d34cf1641911eb28074d6ea032002b9988291f`  
		Last Modified: Thu, 14 May 2026 19:01:35 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35ac7ac8937866df09204157372f3ec18246e1c5bd73c1170045932cfd2ce42`  
		Last Modified: Thu, 14 May 2026 19:01:34 GMT  
		Size: 873.1 KB (873128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65593d14b76d0e9bd2ccc79d323e3f2c9e3b840a42c8842d7f4b6d0726db0069`  
		Last Modified: Thu, 14 May 2026 19:01:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b2db04e90824268a345090fdb0a6b85446a73eb8318eef927f2513ce392ab4`  
		Last Modified: Thu, 14 May 2026 19:01:37 GMT  
		Size: 101.6 MB (101620947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6a3dcefa30e25ebc14aaf3f1d6bd7e0bf4526357f559211b88846b233c6ed6`  
		Last Modified: Thu, 14 May 2026 19:01:35 GMT  
		Size: 9.9 KB (9950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52933c2ac9d3476bae0ad52692d000dad19c05516dd3a12fd5532b206053a977`  
		Last Modified: Thu, 14 May 2026 19:01:36 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8b261da89966594e099d0fe5e3e0dcbc7d7a60db010796215336769b5d06a3`  
		Last Modified: Thu, 14 May 2026 19:01:36 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c813c377707ff223723b8794cd3279f6cb51ac93095d31b3cf3b14c9aa36f2a5`  
		Last Modified: Thu, 14 May 2026 19:01:37 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bfe1acbad4ca3e9cb485ed4720c66bf33237b847a87692d18c4bded4d50c18`  
		Last Modified: Thu, 14 May 2026 19:01:37 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:af26a74591ade665ef8df3193037b386a167049b6c30e8329cdedd053c339034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.6 KB (637596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707530cd06872a070cae2d897c787ae9585be6fb1d072081131224b8062f0174`

```dockerfile
```

-	Layers:
	-	`sha256:975f41dc301bb423d39e4bb17a5e2c5af5750c11230685dcdf4c0485232958eb`  
		Last Modified: Thu, 14 May 2026 19:01:34 GMT  
		Size: 596.3 KB (596347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fba5145f291411cac08046ca3bba5b3f4b6960a8b368cc94165269b54636fb34`  
		Last Modified: Thu, 14 May 2026 19:01:34 GMT  
		Size: 41.2 KB (41249 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:b2bf6c2e44e59dd37eb405f005b3b566848559e524f698605f80ba0b13b23492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116975619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d07bf5d45e902cb1e7be71a5788adea27d07b38d7f7f3fd3a9a64540969e6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 18:58:38 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 18:58:41 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 18:58:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 18:58:41 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 18:58:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 18:58:41 GMT
ENV PG_MAJOR=17
# Thu, 14 May 2026 18:58:41 GMT
ENV PG_VERSION=17.10
# Thu, 14 May 2026 18:58:41 GMT
ENV PG_SHA256=078a03516dcdbdb705fecaf415ea3d13a956c589e46f09fed68a06fb00598c90
# Thu, 14 May 2026 18:58:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:01:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:01:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:01:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:01:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:01:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:01:41 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:01:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:01:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:01:41 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:01:41 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:01:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa95bd5cb0508a4471f5d60f537ee31969bea02e941eb3c809242906d0912908`  
		Last Modified: Thu, 14 May 2026 19:02:00 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93498d37e1d9bb5eb9724f0ee00d8073606f428a7477477da2c13d3ea45aa218`  
		Last Modified: Thu, 14 May 2026 19:02:00 GMT  
		Size: 889.7 KB (889746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a678bea0aaafec9f510c086999af91ddd2be98977b4e6d85d3e141a90c365f`  
		Last Modified: Thu, 14 May 2026 19:01:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fdb27ddc72efed53f2c9afa83830bdf501a88324bfff77708a82d7e9b2e040`  
		Last Modified: Thu, 14 May 2026 19:02:03 GMT  
		Size: 112.4 MB (112443530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7faff0754877a0960320f2463efc9b04173ebf0e98c930b9b868914e14df18`  
		Last Modified: Thu, 14 May 2026 19:02:01 GMT  
		Size: 10.0 KB (9953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d808388afdedf86651917b46637952fb65e18fb2a4400dfa657d98e7f5e6880`  
		Last Modified: Thu, 14 May 2026 19:02:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2b7fd53f5ca4c0818dc16a007e95c0db0ae084986ad86ade3df19fb73e30cd`  
		Last Modified: Thu, 14 May 2026 19:02:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389888e77801e14bbe2359fbfbc06a6e90fed8953ac80429b41b16e51b30e6a6`  
		Last Modified: Thu, 14 May 2026 19:02:02 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776de0e45be44e3f65c37a606829388f985e6c5ddb3e4cbe499d19e3ad2ddb9c`  
		Last Modified: Thu, 14 May 2026 19:02:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:3f1dbe6516d680a633500f077fc6b16838c1d93044e4b6656e127aeae11a7069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.3 KB (637329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b5aba4ef105e6fd7dfe4a61658437b8a3fd5847616796d6382802f2e38ee25`

```dockerfile
```

-	Layers:
	-	`sha256:b3f4a1a378b5b3e5f1faef1b6a640d73cd98ba1263afbbf2df38e9918926e803`  
		Last Modified: Thu, 14 May 2026 19:01:59 GMT  
		Size: 596.3 KB (596300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db45c83d104662923cdbd745d0c52f9dceeb4185ffc5fbb9b1d192e249dd2f64`  
		Last Modified: Thu, 14 May 2026 19:01:59 GMT  
		Size: 41.0 KB (41029 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:afe390f9963915624b2a83233d055e2fc7e8238f9bf036d90d7815dd99b342e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94529041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf13ecada519d257527515b81c328e44ffb1afedfa8398ba5dc900b3db6d59b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 19:32:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 19:32:48 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 19:32:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:32:48 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:32:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:32:48 GMT
ENV PG_MAJOR=17
# Thu, 14 May 2026 19:32:48 GMT
ENV PG_VERSION=17.10
# Thu, 14 May 2026 19:32:48 GMT
ENV PG_SHA256=078a03516dcdbdb705fecaf415ea3d13a956c589e46f09fed68a06fb00598c90
# Thu, 14 May 2026 19:32:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:40:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:40:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:40:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:40:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:40:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:40:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:40:33 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:40:33 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:40:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:40:33 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:40:33 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:40:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063a9d5349dd7c559d9d4da649111e6f9ab000e140d7cddeb891987f33961190`  
		Last Modified: Thu, 14 May 2026 19:36:37 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf0cfbfef73e4ce590e63f32fa324f98af1783d6550c842d675efb1004954ec`  
		Last Modified: Thu, 14 May 2026 19:36:37 GMT  
		Size: 878.3 KB (878314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff9313ecb7b8bbe58328fa20870d086b775001d49958f6112b62cf99f9093b`  
		Last Modified: Thu, 14 May 2026 19:36:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302791e0c244b42f596df568bfd7c6669a7ba98b022a92a70cd66d232f8512fe`  
		Last Modified: Thu, 14 May 2026 19:41:08 GMT  
		Size: 89.9 MB (89896445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2821446dccc572b0304322d7de93b8607865ddc9a5bcd528a6dfa449ebaccf91`  
		Last Modified: Thu, 14 May 2026 19:41:05 GMT  
		Size: 10.0 KB (9955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f55d8ac093f43552cd848956bab6ce9e6872375d4231741b0a818cdf19d238c`  
		Last Modified: Thu, 14 May 2026 19:41:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124902b8a36f0a617fea8fb27c1f23bfb7256669a0aff5ff922fb6d3f9116036`  
		Last Modified: Thu, 14 May 2026 19:41:05 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e8342c3ae3cf1cb0147fb4a60a0d4cb5a1f5fd7d207ca74a7a0fae7ba9ad6f`  
		Last Modified: Thu, 14 May 2026 19:41:06 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7c05354b4e28f7ca2fcf6e6d4e06e3387ad1089d2a344d88c48eadbd03b987`  
		Last Modified: Thu, 14 May 2026 19:41:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:7ca545e20401ada26c9e4c791a408438fd3c3bab6a07b88fb96a62dfc2469062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.8 KB (633829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a46a3548223734abd2128d6f0117380b44018001bc954c99610dac84ad4f40c`

```dockerfile
```

-	Layers:
	-	`sha256:d7710101432575689c8fa930b90ec9abe7359b5c935bdabdccb731730f6896aa`  
		Last Modified: Thu, 14 May 2026 19:41:05 GMT  
		Size: 592.7 KB (592724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ec40c9afb170d64988a42b629185d2695444d63fc4fcf42aff52c48f4dfb2b9`  
		Last Modified: Thu, 14 May 2026 19:41:05 GMT  
		Size: 41.1 KB (41105 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:f42e51434ef296e43aec6a0bfa0490b0870e0569dce54881956a0cfa78d68e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110791192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c253446ec2869069c90490670e96318861bc7bf9453aae590d4ddd8efebcbe8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sat, 16 May 2026 01:21:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 16 May 2026 01:21:54 GMT
ENV GOSU_VERSION=1.19
# Sat, 16 May 2026 01:21:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 16 May 2026 01:21:54 GMT
ENV LANG=en_US.utf8
# Sat, 16 May 2026 01:21:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 16 May 2026 01:21:54 GMT
ENV PG_MAJOR=17
# Sat, 16 May 2026 01:21:54 GMT
ENV PG_VERSION=17.10
# Sat, 16 May 2026 01:21:54 GMT
ENV PG_SHA256=078a03516dcdbdb705fecaf415ea3d13a956c589e46f09fed68a06fb00598c90
# Sat, 16 May 2026 01:21:54 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 16 May 2026 06:15:43 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 16 May 2026 06:15:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 16 May 2026 06:15:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 16 May 2026 06:15:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 16 May 2026 06:15:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sat, 16 May 2026 06:15:45 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 16 May 2026 06:15:45 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 16 May 2026 06:15:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 16 May 2026 06:15:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2026 06:15:45 GMT
STOPSIGNAL SIGINT
# Sat, 16 May 2026 06:15:45 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 16 May 2026 06:15:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fc69dacd00cb4f74d5866a9a0f48ba42062eda649f7e6dfe7b05c76380ca64`  
		Last Modified: Sat, 16 May 2026 02:13:48 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae12ce5ac38eebeb0cdfa7962fc52438d517effb65be9a6ad896b6741b1aef5`  
		Last Modified: Sat, 16 May 2026 02:13:48 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3caea34cdc8633e23fb5e2251e3d24b3207efd8bb627de302d5c5c45a91d790`  
		Last Modified: Sat, 16 May 2026 02:13:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da71187ec16c98f13ba05a6d6e6a1ba3917f0984edb2589385d14f0de489784`  
		Last Modified: Sat, 16 May 2026 06:18:53 GMT  
		Size: 106.4 MB (106386943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325ce6395254ecbb61e7d1eb531c57be0d2143dd19cdcc4563c9823ba45e124b`  
		Last Modified: Sat, 16 May 2026 06:18:37 GMT  
		Size: 10.0 KB (9958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8982b23f2d7c7ee238845246f06a0a835045f4fc8bb5541d306691e84a24a9f`  
		Last Modified: Sat, 16 May 2026 06:18:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f295f03e2ed6bb310bd59abc4de85e854053108a2dd5f6f4146facd33193e856`  
		Last Modified: Sat, 16 May 2026 06:18:37 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779b99b6edf3ec0411dd80347123794530e3a264ca52e034ad387b797b3a4316`  
		Last Modified: Sat, 16 May 2026 06:18:38 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8184162ffbbb760398ee8ade9c96b64f25af19c1650011ec3d2a6aefef74ee6d`  
		Last Modified: Sat, 16 May 2026 06:18:38 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:17687facb820ea9d0f8b52833e3974eab6e5eecf0ddeae9105561a6f682fe19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.5 KB (635492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0061285bb0b40c7ceef012ded42b2e14ada87bd49b39ec6dcea53b92e0b4992`

```dockerfile
```

-	Layers:
	-	`sha256:ba6099624601a16db7a23e2d8d47b78cd5f17fddcfd25d09c19c22da57ed1e64`  
		Last Modified: Sat, 16 May 2026 06:18:37 GMT  
		Size: 594.4 KB (594382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870d2147b8ece4ed87f405d2ba61f337021c960f1e1d1215d9ff9531414fee71`  
		Last Modified: Sat, 16 May 2026 06:18:37 GMT  
		Size: 41.1 KB (41110 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:9720d53d31a2b26a6675fa48eb36898844af7f92c321f2289910280875099dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119410826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b027081a2846c89f19923ef8e3c1dcddd94feeacbfe8c768d183d383b59315f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 18:56:45 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 18:56:48 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 18:56:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 18:56:48 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 18:56:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 18:56:48 GMT
ENV PG_MAJOR=17
# Thu, 14 May 2026 18:56:48 GMT
ENV PG_VERSION=17.10
# Thu, 14 May 2026 18:56:48 GMT
ENV PG_SHA256=078a03516dcdbdb705fecaf415ea3d13a956c589e46f09fed68a06fb00598c90
# Thu, 14 May 2026 18:56:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:14:38 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:14:38 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:14:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:14:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:14:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:14:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:14:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:14:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:14:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:14:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:14:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:14:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e81ceb38917acc4cf3d16bd98043e33a3e2c28415750a8e7da557756eba88c`  
		Last Modified: Thu, 14 May 2026 19:00:13 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ba055b6cddec7c6e4795ffdf5ed7ca4139e686e84c442c3304cfa93062746b`  
		Last Modified: Thu, 14 May 2026 19:00:14 GMT  
		Size: 894.2 KB (894241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97aa08e209ba7c6db28b899b90a123a19c5fde82cded0e06cfd0d21184bb0ca7`  
		Last Modified: Thu, 14 May 2026 19:00:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0070555fbcde462ca168e925a05778932019b305bb171f8c7af0deb8f0ad3258`  
		Last Modified: Thu, 14 May 2026 19:15:11 GMT  
		Size: 114.8 MB (114845092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe60d3420beb0d513c71348fec31fffda9ba4397e539f2c574fbe4025c289312`  
		Last Modified: Thu, 14 May 2026 19:15:03 GMT  
		Size: 10.0 KB (9951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c388b8e2889c55db1308eefa67c08a0f34a2a58ea5c71a4fd61ddd8e4caef063`  
		Last Modified: Thu, 14 May 2026 19:15:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f4dde87ff388c4fca9dc4cf2a83699c0f1da8a454d0ca5e71ad84d8717b4a4`  
		Last Modified: Thu, 14 May 2026 19:15:03 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b0991dc2804e06c548e93743aaa76f7825504aa43eec083406dcef3ffef167`  
		Last Modified: Thu, 14 May 2026 19:15:05 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55d3b217a1e2895374e7a32fddc9ec7cc9998a3af3508b6151cdd0542e7ead9`  
		Last Modified: Thu, 14 May 2026 19:15:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:d06359a075c66c97fc605f4fd350b98e1bed0c7c7967a9da1a216bfd0e86203e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.4 KB (635429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a4a93e3d94b87d734e64de8df1d469cc6e06b996bce09ff0fb322c864c6e43`

```dockerfile
```

-	Layers:
	-	`sha256:d8b22caa9c62f81982d5b6634e5a8c0f8973aaf5da66e530894ecb56f0921fd8`  
		Last Modified: Thu, 14 May 2026 19:15:03 GMT  
		Size: 594.4 KB (594364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f08410493724f25e588df44a3bb86a7e9c29a93388362fcbb5e9f4ffe9783e73`  
		Last Modified: Thu, 14 May 2026 19:15:03 GMT  
		Size: 41.1 KB (41065 bytes)  
		MIME: application/vnd.in-toto+json
