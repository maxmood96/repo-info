## `postgres:alpine3.22`

```console
$ docker pull postgres@sha256:cf70b3d7aeb0f399ba29e94ce081380ccade1f4c38e203309068a30f49548417
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

### `postgres:alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:198c924aa928fecac4bddada3bf4634430aa137a5b1fb577c0d4b6d89a2b1599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113419872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590fab55fbb714b067d02d23dc8c6f62c9b8d76e317236df03d0f4848060e477`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 23:37:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 18 Feb 2026 23:37:33 GMT
ENV GOSU_VERSION=1.19
# Wed, 18 Feb 2026 23:37:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 18 Feb 2026 23:37:33 GMT
ENV LANG=en_US.utf8
# Wed, 18 Feb 2026 23:37:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 18 Feb 2026 23:37:33 GMT
ENV PG_MAJOR=18
# Wed, 18 Feb 2026 23:37:33 GMT
ENV PG_VERSION=18.2
# Wed, 18 Feb 2026 23:37:33 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Wed, 18 Feb 2026 23:37:33 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 18 Feb 2026 23:39:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 18 Feb 2026 23:39:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 18 Feb 2026 23:39:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 18 Feb 2026 23:39:48 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 18 Feb 2026 23:39:48 GMT
VOLUME [/var/lib/postgresql]
# Wed, 18 Feb 2026 23:39:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 23:39:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 18 Feb 2026 23:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 23:39:48 GMT
STOPSIGNAL SIGINT
# Wed, 18 Feb 2026 23:39:48 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 18 Feb 2026 23:39:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74d290bc8a899b8ff545bf39284da3806bca3c6415381f6d107ce4534d0e64d`  
		Last Modified: Wed, 18 Feb 2026 23:40:03 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a88cb62c3ac6749d4547960e10a7932624331de7da12c948fba27e0f2a5095`  
		Last Modified: Wed, 18 Feb 2026 23:40:03 GMT  
		Size: 918.3 KB (918290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea573d06220ab28e04945a908baa237982f4d86b9a0ecc10790e62e022f859e`  
		Last Modified: Wed, 18 Feb 2026 23:40:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17aa8efe79aa8505b30777796cb301d2ac158f66b6c874db533e532f95777523`  
		Last Modified: Wed, 18 Feb 2026 23:40:06 GMT  
		Size: 108.7 MB (108670541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49980ab1d1895dbd84e5184554562ce5ee75efcd2220dad2a77c59efaa31427f`  
		Last Modified: Wed, 18 Feb 2026 23:40:04 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5917cd2dbd52736d40cb18e793eb7e573cf123e993e58ec25ca4e2ffc2c30b3`  
		Last Modified: Wed, 18 Feb 2026 23:40:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988beb9e76a53dc4af4c320667d063e0ca53468b39e07ff7312d8ccbad7470c4`  
		Last Modified: Wed, 18 Feb 2026 23:40:04 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296616ec4ece2fc6ee6e5dfae8e5e81faf2d38bb09d83e41dff101c4efb8a15c`  
		Last Modified: Wed, 18 Feb 2026 23:40:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:461dc331133701492c068479d5f0c4317b952149b76000135d2310a0baf189a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.3 KB (655318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe52644f201cd2be5cc11652a38b02a5d7677a03c800f9b93eafe574a8f2b58`

```dockerfile
```

-	Layers:
	-	`sha256:320f78e50cfb5afc9e2fa8e1e528dc284627d9507681dd1ef5724174d93ec315`  
		Last Modified: Wed, 18 Feb 2026 23:40:03 GMT  
		Size: 615.2 KB (615192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac21ad9e9500cb8f34c11e1e4013c4165683841705bd4912382bc5fbd3c55e36`  
		Last Modified: Wed, 18 Feb 2026 23:40:03 GMT  
		Size: 40.1 KB (40126 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:fec1dec229e457b80e879f169cb7f0faf0c3506080686666da6c13a498b2677b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92936549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d0779830bfbad0b1d221cb9fb5b268fb19642b18bca34e8a630c9e9ba09d54e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 23:38:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 18 Feb 2026 23:38:54 GMT
ENV GOSU_VERSION=1.19
# Wed, 18 Feb 2026 23:38:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 18 Feb 2026 23:38:54 GMT
ENV LANG=en_US.utf8
# Wed, 18 Feb 2026 23:38:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 18 Feb 2026 23:38:54 GMT
ENV PG_MAJOR=18
# Wed, 18 Feb 2026 23:38:54 GMT
ENV PG_VERSION=18.2
# Wed, 18 Feb 2026 23:38:54 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Wed, 18 Feb 2026 23:38:54 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 18 Feb 2026 23:42:02 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 18 Feb 2026 23:42:02 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 18 Feb 2026 23:42:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 18 Feb 2026 23:42:02 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 18 Feb 2026 23:42:02 GMT
VOLUME [/var/lib/postgresql]
# Wed, 18 Feb 2026 23:42:02 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 23:42:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 18 Feb 2026 23:42:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 23:42:02 GMT
STOPSIGNAL SIGINT
# Wed, 18 Feb 2026 23:42:02 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 18 Feb 2026 23:42:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344f5df7c139999c98b7538859b06ee5db80c87aff8a4c4c45b967d64a4b9dee`  
		Last Modified: Wed, 18 Feb 2026 23:42:13 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e888d2f30e89901b868beda0d2c7f1098fb356056cf1221cf3bb6f78c40dcf`  
		Last Modified: Wed, 18 Feb 2026 23:42:12 GMT  
		Size: 886.1 KB (886133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3a8b670bb56c0586eefe64fa292decaa07effd36b730d781d71155114cea12`  
		Last Modified: Wed, 18 Feb 2026 23:42:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d160b44d40f5990e7b9b8d774e280a0ef86625863ecaf69e6ddb70563be0a55e`  
		Last Modified: Wed, 18 Feb 2026 23:42:14 GMT  
		Size: 88.5 MB (88519213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d32244cf6dda6f62dfebf2745d4a9a9f6a81e59201571e5172533284c3ea9ac`  
		Last Modified: Wed, 18 Feb 2026 23:42:14 GMT  
		Size: 18.9 KB (18919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0cb03ae976c635d6081b77b03c83fc7fae972f7df102b98a24259906e9b0cd`  
		Last Modified: Wed, 18 Feb 2026 23:42:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b288305ca2ba6e09e5101995b020a3ac99952b5c4dd2d173a56f890699f3f1a`  
		Last Modified: Wed, 18 Feb 2026 23:42:14 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a19289b88d67b484a608931f08a19189dcc83ee7ffca708a27d73ed36b92e97`  
		Last Modified: Wed, 18 Feb 2026 23:42:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:9f98cddd007a78cf62200005b28f382b460a3361e5183ae283eb340b61f634d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0944739643db3539d5603090ce3198d6cb34c5a489268c8e1934f49921fbb0ef`

```dockerfile
```

-	Layers:
	-	`sha256:ad2361a13ef6dbd0928f8732c0e4126163fe33c0d703ace6659d7f190279eb81`  
		Last Modified: Wed, 18 Feb 2026 23:42:12 GMT  
		Size: 40.1 KB (40056 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:a02099ee4909f6efc7a74450b501ca09b0a6d08a1cd602151541dca3528cb693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88047642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1be35335cb23542ba4f62988174867cf298a56b4f5151b7368096e5bc96516f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 23:35:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 18 Feb 2026 23:35:25 GMT
ENV GOSU_VERSION=1.19
# Wed, 18 Feb 2026 23:35:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 18 Feb 2026 23:35:25 GMT
ENV LANG=en_US.utf8
# Wed, 18 Feb 2026 23:35:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 18 Feb 2026 23:35:25 GMT
ENV PG_MAJOR=18
# Wed, 18 Feb 2026 23:35:25 GMT
ENV PG_VERSION=18.2
# Wed, 18 Feb 2026 23:35:25 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Wed, 18 Feb 2026 23:35:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 18 Feb 2026 23:38:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 18 Feb 2026 23:38:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 18 Feb 2026 23:38:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 18 Feb 2026 23:38:16 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 18 Feb 2026 23:38:16 GMT
VOLUME [/var/lib/postgresql]
# Wed, 18 Feb 2026 23:38:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 23:38:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 18 Feb 2026 23:38:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 23:38:16 GMT
STOPSIGNAL SIGINT
# Wed, 18 Feb 2026 23:38:16 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 18 Feb 2026 23:38:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6430d575dd1d8f232741ad848777bf53205d704ef10a4da5b07210a456122adf`  
		Last Modified: Wed, 18 Feb 2026 23:38:28 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9927d0c2db06a4b5670c8e3d19bbfc664a3425eb3467795e75b7d9be32ab01`  
		Last Modified: Wed, 18 Feb 2026 23:38:28 GMT  
		Size: 886.1 KB (886134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9db68b4468e66696fc6d36324ce9682ca9061521f892f3eff416703989130fe`  
		Last Modified: Wed, 18 Feb 2026 23:38:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19fe0311fb09b7167ce97a6f77aa2882a83ceb21a67df1c53db3386617bf3b9`  
		Last Modified: Wed, 18 Feb 2026 23:38:30 GMT  
		Size: 83.9 MB (83911720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297d23ad7ad96f28d9d20ea52cf50eed38f0043cdad2d0cf092d50b9f354ac5d`  
		Last Modified: Wed, 18 Feb 2026 23:38:29 GMT  
		Size: 18.9 KB (18920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca87f7cd31d55c52f8b6d909218ae90f54d5361d5e196471c60c6f75c598ddaf`  
		Last Modified: Wed, 18 Feb 2026 23:38:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b302efa958f54ebb0a41e83352f04eba4a9e02cdabaa4cc30df6b79b201f981`  
		Last Modified: Wed, 18 Feb 2026 23:38:30 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97bfb173ff1ad3f38fd392275c6a134f58ac2739331173c88630027c5ac2dff`  
		Last Modified: Wed, 18 Feb 2026 23:38:30 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:d4e0fbd49d473c148f1c1eb844471ec209d7ceb19b6ffc1fb65dede2af1b8675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.5 KB (655490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27126cfdfcc121e8d20f8d8be67d64c92fd0d65416496b4627da53a53d0900c2`

```dockerfile
```

-	Layers:
	-	`sha256:a4c5b8d883ad7a6cad5034c8c13b4d8b3f38db0d26dd9acc2d1b8084907f4f05`  
		Last Modified: Wed, 18 Feb 2026 23:38:28 GMT  
		Size: 615.2 KB (615220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4445e9f0a2f5f91585795cd50d77e07af4cc8fda6379c8c4011dcadec8298fc5`  
		Last Modified: Wed, 18 Feb 2026 23:38:28 GMT  
		Size: 40.3 KB (40270 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:e0d54133019e79da6d2977da52651f7d22109436d730a5be2ea1c4eda24b5dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109405309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33bba415af54ac173ae1911cb7336a1502290ecceb8c5385e94bfcbe7c81585`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 23:37:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 18 Feb 2026 23:37:09 GMT
ENV GOSU_VERSION=1.19
# Wed, 18 Feb 2026 23:37:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 18 Feb 2026 23:37:09 GMT
ENV LANG=en_US.utf8
# Wed, 18 Feb 2026 23:37:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 18 Feb 2026 23:37:09 GMT
ENV PG_MAJOR=18
# Wed, 18 Feb 2026 23:37:09 GMT
ENV PG_VERSION=18.2
# Wed, 18 Feb 2026 23:37:09 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Wed, 18 Feb 2026 23:37:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 18 Feb 2026 23:39:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 18 Feb 2026 23:39:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 18 Feb 2026 23:39:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 18 Feb 2026 23:39:32 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 18 Feb 2026 23:39:32 GMT
VOLUME [/var/lib/postgresql]
# Wed, 18 Feb 2026 23:39:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 23:39:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 18 Feb 2026 23:39:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 23:39:32 GMT
STOPSIGNAL SIGINT
# Wed, 18 Feb 2026 23:39:32 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 18 Feb 2026 23:39:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84993984bbd399bdcf021c91af597f224aac8dd3f2c2c94be31c4b0e31b4f756`  
		Last Modified: Wed, 18 Feb 2026 23:39:47 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aba87412f40cdbd8861dd67acdcf2b4d65cb0c15a7d42a53260c22805b8696f`  
		Last Modified: Wed, 18 Feb 2026 23:39:47 GMT  
		Size: 873.5 KB (873484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a46014ca94bf3bdcf88191c3eb8f3902fe63ee9d1f7b8867c78538dc95ec5a`  
		Last Modified: Wed, 18 Feb 2026 23:39:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c04de3eefb26583f20b96f164ed366d3ecba1460731a9267336003a8a8f6907`  
		Last Modified: Wed, 18 Feb 2026 23:39:50 GMT  
		Size: 104.4 MB (104366147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0337bb4879d771263514e0ad3524ac978bcc8d83df4dd006ee8b712df45c431`  
		Last Modified: Wed, 18 Feb 2026 23:39:48 GMT  
		Size: 18.9 KB (18919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025f8c53614f989f7d2ec212a948ffe5b26f8b52ff35a105c75da2bc0203821c`  
		Last Modified: Wed, 18 Feb 2026 23:39:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17069efe69ddab7f1928a88e870b7c9276cb921c7f097a580bcccc999ebc2ccd`  
		Last Modified: Wed, 18 Feb 2026 23:39:48 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b214d50d9c84dd716268c905fe5d9f063690a106bac904d51dbbf053c165d88`  
		Last Modified: Wed, 18 Feb 2026 23:39:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:a7d37eed5d0533426ac1894db487d925fbeba75c2799682d1541138cdec29125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.5 KB (655544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c85e92a83e18f6b7336928ef28781cc3cebd40b2f9e0467aeb1313e328f979`

```dockerfile
```

-	Layers:
	-	`sha256:937e79eb24a88d1721b26aacc48f20cdc943c64c5e334fb676e3f2c60f2e0587`  
		Last Modified: Wed, 18 Feb 2026 23:39:47 GMT  
		Size: 615.2 KB (615236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb26288e571aa40cc971db0b4be45f9a3c56a93d069318cb71699b99f246bc8`  
		Last Modified: Wed, 18 Feb 2026 23:39:47 GMT  
		Size: 40.3 KB (40308 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:27f2a3851b5b8ea9db9dc55c137b7855a20b2e6f419432b0ea60bff498fada57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119828919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6d05053c91e974742423ca037a54c44e2ef1d88aa5c356b537cb25df8a54f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 23:37:49 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 18 Feb 2026 23:37:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 18 Feb 2026 23:37:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 18 Feb 2026 23:37:55 GMT
ENV LANG=en_US.utf8
# Wed, 18 Feb 2026 23:37:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 18 Feb 2026 23:37:55 GMT
ENV PG_MAJOR=18
# Wed, 18 Feb 2026 23:37:55 GMT
ENV PG_VERSION=18.2
# Wed, 18 Feb 2026 23:37:55 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Wed, 18 Feb 2026 23:37:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 18 Feb 2026 23:41:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 18 Feb 2026 23:41:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 18 Feb 2026 23:41:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 18 Feb 2026 23:41:07 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 18 Feb 2026 23:41:07 GMT
VOLUME [/var/lib/postgresql]
# Wed, 18 Feb 2026 23:41:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 23:41:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 18 Feb 2026 23:41:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 23:41:07 GMT
STOPSIGNAL SIGINT
# Wed, 18 Feb 2026 23:41:07 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 18 Feb 2026 23:41:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5717b9a49f3d28b02547ae42914fb481e9c3e91e2332ae7c217388d48b2715`  
		Last Modified: Wed, 18 Feb 2026 23:41:23 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d541ec38a207830ee56915abd7a72a1506ff29b2f75c17808e9b12712cc219fb`  
		Last Modified: Wed, 18 Feb 2026 23:41:23 GMT  
		Size: 890.6 KB (890636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b77ff719475c552c14fd941cc292d5d5bd8cf6c0fe3850fe853493efd22c96`  
		Last Modified: Wed, 18 Feb 2026 23:41:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0c3e520c0aebaf8791760e8bf706b11bd4b594b9990577faae0df5d1f520a9`  
		Last Modified: Wed, 18 Feb 2026 23:41:26 GMT  
		Size: 115.3 MB (115291393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf61f0393fab431ac2f32faf81f6f9226385bebb2214bc3aa1bcfecf0b6557f`  
		Last Modified: Wed, 18 Feb 2026 23:41:24 GMT  
		Size: 18.9 KB (18917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f2ecbd7deadf57da0b1ae2e1ed264140d6edaa5a5055dfe6e0251e0dc209ca`  
		Last Modified: Wed, 18 Feb 2026 23:41:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c43e185cca011cdf0e804cf0355e3e34f65edede96116b7a5459163a3640a0`  
		Last Modified: Wed, 18 Feb 2026 23:41:24 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e68f33cea97fa7d7e07e0943ef1915391f45589c7d8ae1b553b00dab94494f`  
		Last Modified: Wed, 18 Feb 2026 23:41:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:7b0a605bf82f53214651a1ad6080ba32fda88cdd93bea8b808b5734e03b6b73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.3 KB (655259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ddf827e7ff2164a2c1ad270cf69bab0b3ce3d8512565c69a73d4369901a547`

```dockerfile
```

-	Layers:
	-	`sha256:90306b96783b2b3092ffa7ae5caadc89620986242d8decbd61957fa576b062f3`  
		Last Modified: Wed, 18 Feb 2026 23:41:23 GMT  
		Size: 615.2 KB (615172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0cfee8234a279551af0d11e6c6b3d5453e943101292bcb70e210766ffe05f5c`  
		Last Modified: Wed, 18 Feb 2026 23:41:23 GMT  
		Size: 40.1 KB (40087 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:50fca9b971939590dcd89f03c4302ed8a3368f7d482216701245554a56504855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97439293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9fb3f54f927db753a6cc8253b3d119ed9fd2005233cfe1a259e2c78033f0c28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:06:00 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:06:12 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:06:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:06:12 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:06:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:06:12 GMT
ENV PG_MAJOR=18
# Thu, 12 Feb 2026 21:06:12 GMT
ENV PG_VERSION=18.2
# Thu, 12 Feb 2026 21:06:12 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Thu, 12 Feb 2026 21:06:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 18 Feb 2026 23:39:35 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 18 Feb 2026 23:39:35 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 18 Feb 2026 23:39:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 18 Feb 2026 23:39:36 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 18 Feb 2026 23:39:36 GMT
VOLUME [/var/lib/postgresql]
# Wed, 18 Feb 2026 23:39:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 23:39:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 18 Feb 2026 23:39:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 23:39:37 GMT
STOPSIGNAL SIGINT
# Wed, 18 Feb 2026 23:39:37 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 18 Feb 2026 23:39:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c65175e4a78e75c1adc1c569354fe719e50457fdbdd1612adccbd559da08c1`  
		Last Modified: Thu, 12 Feb 2026 21:11:11 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47af42dfcd093de1f52666dfa1cb8ed4291e124998435eea188cac1feb2ef729`  
		Last Modified: Thu, 12 Feb 2026 21:11:11 GMT  
		Size: 879.0 KB (879036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8773caba0cc71f1241c5d1fb6e8c3b7afa6a89200a7975c71ffbf3112756a3`  
		Last Modified: Thu, 12 Feb 2026 21:11:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40a94656bc9903f168dd877e044e28a9cb2e3b7e0e5bea5d54652ab81740b53`  
		Last Modified: Wed, 18 Feb 2026 23:40:21 GMT  
		Size: 92.8 MB (92799792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ae8e007f844fcf7ee2eb4b1b67a3999bd78d7c3adff8d046a0aa6224c92a2c`  
		Last Modified: Wed, 18 Feb 2026 23:40:18 GMT  
		Size: 18.9 KB (18922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb68c9ea695cdbba1d38b214793abf5b5c54f303e22a202ace0e17d0dfa82f5e`  
		Last Modified: Wed, 18 Feb 2026 23:40:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a14be5cfc366f3efe13d11924241338a5f66ab0d38e250837fa03df71ae1c64`  
		Last Modified: Wed, 18 Feb 2026 23:40:18 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4177ec004f8a565b9afedc392f247f28155c00611fbbafa3fec0a87e9b25b33c`  
		Last Modified: Wed, 18 Feb 2026 23:40:19 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:ff5f468099491b61f611f9ba4090ce185bdc880319646bee4462c53541fc486f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.8 KB (651777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a6152617cd84e929a5cc02512604b21ee635b9cb563589fdf2061e73b18d95`

```dockerfile
```

-	Layers:
	-	`sha256:8f9f5297d840667d0738e303936b8b0ac57c952a1f1aa82dc1957da0302e4867`  
		Last Modified: Wed, 18 Feb 2026 23:40:18 GMT  
		Size: 611.6 KB (611607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a2f59b80023038378654ed8bcaaa9eee0dd03064ca01b92511e44c7a5f7e1cf`  
		Last Modified: Wed, 18 Feb 2026 23:40:18 GMT  
		Size: 40.2 KB (40170 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:bb0c179702c8e461a75caa4e9a19868b2e4ee7e209b833692bb928c0e275129b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.7 MB (113689634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317106c0c2a499ae21426735c24860e28e5bdf752c33036a7ad612b1216bf134`
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
# Fri, 13 Feb 2026 00:03:22 GMT
ENV LANG=en_US.utf8
# Fri, 13 Feb 2026 00:03:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 13 Feb 2026 00:03:22 GMT
ENV PG_MAJOR=18
# Fri, 13 Feb 2026 00:03:22 GMT
ENV PG_VERSION=18.2
# Fri, 13 Feb 2026 00:03:22 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Fri, 13 Feb 2026 00:03:22 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 19 Feb 2026 01:19:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 19 Feb 2026 01:19:29 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 19 Feb 2026 01:19:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 19 Feb 2026 01:19:29 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 19 Feb 2026 01:19:29 GMT
VOLUME [/var/lib/postgresql]
# Thu, 19 Feb 2026 01:19:29 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 01:19:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 19 Feb 2026 01:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 01:19:29 GMT
STOPSIGNAL SIGINT
# Thu, 19 Feb 2026 01:19:29 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 19 Feb 2026 01:19:29 GMT
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
	-	`sha256:778a0da493e5086a70feef9ef732427bd2c927a4c5e0b6cb88e9e6e2f5d4d72a`  
		Last Modified: Fri, 13 Feb 2026 00:55:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e585f51b923a2206d566b5817373ad4c82ba71df592bc039a94aa9a8ba6d0873`  
		Last Modified: Thu, 19 Feb 2026 01:22:41 GMT  
		Size: 109.3 MB (109279415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1906f852d75ec2148713b057cdc5abfb82fc80581cfba3b1ecc8b87ca3b7476`  
		Last Modified: Thu, 19 Feb 2026 01:22:24 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eed10fae7e77f531d14f6b71ee8d6d8a064fd0c6095e31f1699b576aadccc5`  
		Last Modified: Thu, 19 Feb 2026 01:22:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36a4555cb443ff9246a187ccb594aea846d244c4409723bdc4b76ebf0c03540`  
		Last Modified: Thu, 19 Feb 2026 01:22:24 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc73e41997cab959818011921e046730171f8ebdec8f8b7b3ef1ebe76c391c98`  
		Last Modified: Thu, 19 Feb 2026 01:22:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:add2cc8919c79caa91fce62c0916704905d6d04e6d90ac24646f2ae041c57970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.4 KB (653441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5974f16591301f455307e53d8e86179405244ee9f02b6c6d472c3ac9744d16b`

```dockerfile
```

-	Layers:
	-	`sha256:e99e0e59cbfa649d49fba50b98074b8dd91337c71d7d72f147378b66ffe50992`  
		Last Modified: Thu, 19 Feb 2026 01:22:24 GMT  
		Size: 613.3 KB (613265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbcc15db8dce75bdb131a70c0d55507917675d95f479c150375fe159ffab1ec5`  
		Last Modified: Thu, 19 Feb 2026 01:22:24 GMT  
		Size: 40.2 KB (40176 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:362d2105e948f4e47d971185a45f0554e4e779081f5651c1a9de8934f0cdc9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122314564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe2f10b26f2212755462a80072a00b2891472709aa7aa68d7446230b4323f2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 23:34:58 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 18 Feb 2026 23:35:04 GMT
ENV GOSU_VERSION=1.19
# Wed, 18 Feb 2026 23:35:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 18 Feb 2026 23:35:04 GMT
ENV LANG=en_US.utf8
# Wed, 18 Feb 2026 23:35:04 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 18 Feb 2026 23:35:04 GMT
ENV PG_MAJOR=18
# Wed, 18 Feb 2026 23:35:04 GMT
ENV PG_VERSION=18.2
# Wed, 18 Feb 2026 23:35:04 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Wed, 18 Feb 2026 23:35:04 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 18 Feb 2026 23:38:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 18 Feb 2026 23:38:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 18 Feb 2026 23:38:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 18 Feb 2026 23:38:49 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 18 Feb 2026 23:38:49 GMT
VOLUME [/var/lib/postgresql]
# Wed, 18 Feb 2026 23:38:49 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 23:38:50 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 18 Feb 2026 23:38:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 23:38:50 GMT
STOPSIGNAL SIGINT
# Wed, 18 Feb 2026 23:38:50 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 18 Feb 2026 23:38:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390f114ddda0a936ceae7682653057edba273a5369ef335ab7bb39ccca30d5be`  
		Last Modified: Wed, 18 Feb 2026 23:39:24 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8890a3f16efedfe37b3192f6198b87061845e82d9e99cee82febe194917d65`  
		Last Modified: Wed, 18 Feb 2026 23:39:24 GMT  
		Size: 894.4 KB (894417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599964ccc076974e7084f5730e574777aa95e209f3eae119bbf35d459408129a`  
		Last Modified: Wed, 18 Feb 2026 23:39:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b393aff538bdd1e87af59a287826eee7d5c080554e001f35526f83dcbe181084`  
		Last Modified: Wed, 18 Feb 2026 23:39:26 GMT  
		Size: 117.7 MB (117743542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1781dd2464e39e4aa0ee9042704a71ac73566be99676824ee8f8ef7cdca1df72`  
		Last Modified: Wed, 18 Feb 2026 23:39:25 GMT  
		Size: 18.9 KB (18925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306f24465eaacdf8783431f54f7e7944d9aa5d9833c9d1e7c0f2f33c8d0c9075`  
		Last Modified: Wed, 18 Feb 2026 23:39:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ad8e50521da295434733d733f381fec7ceacb55fce86777ed5fcdc4b3abee8`  
		Last Modified: Wed, 18 Feb 2026 23:39:25 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5c4620b978949279a9ff88e52cc3b9351a34394ebc05baae81803bf7675f98`  
		Last Modified: Wed, 18 Feb 2026 23:39:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:bd9da998fc784be53e656088a70028fa56b165c4c21b4f14873c079c09aa1828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.4 KB (653366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417191981afd51361d9a03f124303b0e414b111795d1d0133803727f33597937`

```dockerfile
```

-	Layers:
	-	`sha256:48b71b945e043c4c1fabcd62a42212446a54f40400e12b3a9e16a725584cc141`  
		Last Modified: Wed, 18 Feb 2026 23:39:24 GMT  
		Size: 613.2 KB (613241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac908cde1e424e11ab94656f9a989911098c78da9e3805803c829f12468be51`  
		Last Modified: Wed, 18 Feb 2026 23:39:24 GMT  
		Size: 40.1 KB (40125 bytes)  
		MIME: application/vnd.in-toto+json
