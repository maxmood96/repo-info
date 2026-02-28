## `postgres:alpine3.22`

```console
$ docker pull postgres@sha256:cd50a785da60925f8f6b59fdf680ae0a10dc96392d5bda489af12d945986dd78
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
$ docker pull postgres@sha256:8e92eef28941ff415cde86f9edcb8d3eb69b0b499b50b9b7463cb091a55eca1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113420076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8977b33820819ee3ad4aa7272b9b7e3c557895e23a144f766ced3b331e3721`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:23:21 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:23:24 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:23:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:23:24 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:23:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:23:24 GMT
ENV PG_MAJOR=18
# Thu, 26 Feb 2026 19:23:24 GMT
ENV PG_VERSION=18.3
# Thu, 26 Feb 2026 19:23:24 GMT
ENV PG_SHA256=d95663fbbf3a80f81a9d98d895266bdcb74ba274bcc04ef6d76630a72dee016f
# Thu, 26 Feb 2026 19:23:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:25:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:25:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:25:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:25:58 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 26 Feb 2026 19:25:58 GMT
VOLUME [/var/lib/postgresql]
# Thu, 26 Feb 2026 19:25:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:25:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:25:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:25:58 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:25:58 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:25:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225f399e2214b2e7d074c8eb93fef7fd9f565df8d2e8022271cb8bee79346c3d`  
		Last Modified: Thu, 26 Feb 2026 19:26:14 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1c922580b8dd35d5d33927521562857646dc429b680bca27632ec106ee16e5`  
		Last Modified: Thu, 26 Feb 2026 19:26:14 GMT  
		Size: 918.3 KB (918290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d0b405bf6ac163bdacbd0635b7db3add327929d1f1b3ea83f1d620276999da`  
		Last Modified: Thu, 26 Feb 2026 19:26:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b24c0be03916b56078e8420cd66c3762188d44bd5f31f423805531a3a64ff0`  
		Last Modified: Thu, 26 Feb 2026 19:26:17 GMT  
		Size: 108.7 MB (108670748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981051bdfdcd566f109133bd8b06918b086284430816fe34cc9eb4ef946bea82`  
		Last Modified: Thu, 26 Feb 2026 19:26:15 GMT  
		Size: 18.9 KB (18919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac4626f066f5f3b29df0bd1917223ee0e278cea92cbe2f025bf1e9d869434f8`  
		Last Modified: Thu, 26 Feb 2026 19:26:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5227b1d31f1868f8300bf90137f2e66b0aa39a3e161362d10bce53af16eec9f4`  
		Last Modified: Thu, 26 Feb 2026 19:26:16 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e0eacfde731a84880e6c4239081853f41746ffb06da35a385a5b7e81607d53`  
		Last Modified: Thu, 26 Feb 2026 19:26:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:f2078cb773a5afd568cd5c5d6203eb9b1fbdb6bf9399c0162f60bc31435e8902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.3 KB (655318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:570ec17571f1508248042ed7567d7508c35ab6b5577a1be707c1a00ab13bcacb`

```dockerfile
```

-	Layers:
	-	`sha256:70c263811d53685b0f70ab6de128bf84cfc570b296d8b93ce5709304670a8b7e`  
		Last Modified: Thu, 26 Feb 2026 19:26:14 GMT  
		Size: 615.2 KB (615192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92b908ec1f776c28b0eb42929c9d65b2a2a352e54c1204c1c741a5ed659dedb4`  
		Last Modified: Thu, 26 Feb 2026 19:26:14 GMT  
		Size: 40.1 KB (40126 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:28e6591309f50ada94a10dcceeab4b387b5d6e924374dc1b1acab123ccff8567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92936102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a87c0526a97e0642140aee69f39f6cdc374ae754f4b389f56c2163a10f55d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:15:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:15:38 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:15:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:15:38 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:15:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:15:39 GMT
ENV PG_MAJOR=18
# Thu, 26 Feb 2026 19:15:39 GMT
ENV PG_VERSION=18.3
# Thu, 26 Feb 2026 19:15:39 GMT
ENV PG_SHA256=d95663fbbf3a80f81a9d98d895266bdcb74ba274bcc04ef6d76630a72dee016f
# Thu, 26 Feb 2026 19:15:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:18:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:18:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:18:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:18:42 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 26 Feb 2026 19:18:42 GMT
VOLUME [/var/lib/postgresql]
# Thu, 26 Feb 2026 19:18:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:18:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:18:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:18:42 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:18:42 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:18:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253c7b2562cec0e5c2584ec3d9799036e99fa54cd2f39912b710d74e8913dd49`  
		Last Modified: Thu, 26 Feb 2026 19:18:52 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf04899b67bdc98e11ac34edcfa6dfe66d086a2250c445a77a538c3fd4485460`  
		Last Modified: Thu, 26 Feb 2026 19:18:52 GMT  
		Size: 886.1 KB (886132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a517c3f326e42cd7a58b9f548087803f41052d84f9934fcd94d5cc0c7aa25e41`  
		Last Modified: Thu, 26 Feb 2026 19:18:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae0bb81973013155f90649e623f0bd759ed05897410a496d153bffd14e28eda`  
		Last Modified: Thu, 26 Feb 2026 19:18:58 GMT  
		Size: 88.5 MB (88518770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71df64ea6950bc5b5fd636990ce8d07a03bbc261d97c8e9dda1c0fad064a4bef`  
		Last Modified: Thu, 26 Feb 2026 19:18:53 GMT  
		Size: 18.9 KB (18917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dbff30f0b38fc4f7d154d20aafbae64950089b2b97ceb6ee9a28289a7f10cf`  
		Last Modified: Thu, 26 Feb 2026 19:18:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca447e7d8ad41176d54d4205b839795a7ccdb4df5b3f945f91c66fe6077182e`  
		Last Modified: Thu, 26 Feb 2026 19:18:54 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6194076c58e471b7af57d1cc1ac23d634bbad2039ad9950ebab412f906fa34f`  
		Last Modified: Thu, 26 Feb 2026 19:18:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:f0d876f8cac858624fe3bdebb4c99f36f005dd19707b3b33a20aba512d157dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5364481b2b67272226c0ee653f48e2d2109b9a2630c1095e0a43e571f1632d7a`

```dockerfile
```

-	Layers:
	-	`sha256:0690196daf6271eec71595335d3328810b081e40c8a7bc53d1cd2590b68844ed`  
		Last Modified: Thu, 26 Feb 2026 19:18:52 GMT  
		Size: 40.1 KB (40055 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:d3238f95ea5cabf584afb9681a90bc65f919f77e75b0cdf7eaf8984bfff64bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88047107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605039486a7ed0f7ef7bab27df45ae546846ec9709378e66ec41361ad47116bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:19:21 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:19:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:19:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:19:29 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:19:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:19:29 GMT
ENV PG_MAJOR=18
# Thu, 26 Feb 2026 19:19:29 GMT
ENV PG_VERSION=18.3
# Thu, 26 Feb 2026 19:19:29 GMT
ENV PG_SHA256=d95663fbbf3a80f81a9d98d895266bdcb74ba274bcc04ef6d76630a72dee016f
# Thu, 26 Feb 2026 19:19:29 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:22:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:22:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:22:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:22:23 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 26 Feb 2026 19:22:23 GMT
VOLUME [/var/lib/postgresql]
# Thu, 26 Feb 2026 19:22:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:22:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:22:23 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:22:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:22:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886d0bb941000456db0930458ee64dc86eef2f9a5351eb8fa6f4296ea4e446f2`  
		Last Modified: Thu, 26 Feb 2026 19:22:36 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5088b8f22a045b02976ee35fe960e5a7f94d5660a11400310f91a9f36479a54`  
		Last Modified: Thu, 26 Feb 2026 19:22:35 GMT  
		Size: 886.1 KB (886140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bc55c62d743bbebabd418ce33d92b14e61fe342ca394429818c1764d1bf617`  
		Last Modified: Thu, 26 Feb 2026 19:22:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242344eda2f9e2a1ae68c7ac8fdb00a3b65d5c5ce2248bb4301cd1e67821ffe2`  
		Last Modified: Thu, 26 Feb 2026 19:22:38 GMT  
		Size: 83.9 MB (83911185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cd901bc614ec0cfa3b6ac41edb0def79d265222bb7ce7360f2510c1d3712a0`  
		Last Modified: Thu, 26 Feb 2026 19:22:36 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eadb325ffe06882f1573796d8b4bbe33eec330b3371e962d58c34983d79b0ed`  
		Last Modified: Thu, 26 Feb 2026 19:22:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608cc4c6d6efb6515c69d6980f39057965cef3dfc22e5ac97bced52854ab1958`  
		Last Modified: Thu, 26 Feb 2026 19:22:37 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8444c13e2de701ac4c0d6b59140eddc1fd8e4cc07746086357f708cd5d6081c4`  
		Last Modified: Thu, 26 Feb 2026 19:22:38 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:177faaed3749f282e78cc91c41f0387c7ac550ad49e640ae08fbaa6baf62479b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.5 KB (655491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a78c8499a7d00c9a92a8b8f0fb19e48dc7c4008d52a8a934f60896753bcda1d`

```dockerfile
```

-	Layers:
	-	`sha256:2f03e2a2763346dfd3f634d7b399f1de5f776276e83782c3100203a548d7a085`  
		Last Modified: Thu, 26 Feb 2026 19:22:35 GMT  
		Size: 615.2 KB (615220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1cb88d5b3b08048bfea2367772940b997eb7dafa9c209284ad836ae90b8cfeb`  
		Last Modified: Thu, 26 Feb 2026 19:22:35 GMT  
		Size: 40.3 KB (40271 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:b15267fd4f18364431586ce12690da61bc87b93218be31a3482b662df2302cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109407096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8334df66842548ae1af2f3db5d18c4d1caddf823fc869e7ea1de9be7388e6ed4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:21:42 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:21:45 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:21:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:21:45 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:21:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:21:45 GMT
ENV PG_MAJOR=18
# Thu, 26 Feb 2026 19:21:45 GMT
ENV PG_VERSION=18.3
# Thu, 26 Feb 2026 19:21:45 GMT
ENV PG_SHA256=d95663fbbf3a80f81a9d98d895266bdcb74ba274bcc04ef6d76630a72dee016f
# Thu, 26 Feb 2026 19:21:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:24:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:24:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:24:15 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:24:15 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 26 Feb 2026 19:24:15 GMT
VOLUME [/var/lib/postgresql]
# Thu, 26 Feb 2026 19:24:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:24:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:24:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:24:16 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:24:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:24:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e94fdc345c78ea1396153d22ac7e05f08d16a4bc58acb96a5a99eeee91ee784`  
		Last Modified: Thu, 26 Feb 2026 19:24:30 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6b9e22bba3418905b8996c8872273a342cca9677d9de3cea817ca96f602d5e`  
		Last Modified: Thu, 26 Feb 2026 19:24:30 GMT  
		Size: 873.5 KB (873491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec4cbdb16774e35569e183da3e59d4a44b1203f03d7cdbd6e72018d967fc9f7`  
		Last Modified: Thu, 26 Feb 2026 19:24:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bffa3882fdbfe4c72290526ca3ce6fa74ebd32f37709cba3863dd5a87391da5`  
		Last Modified: Thu, 26 Feb 2026 19:24:33 GMT  
		Size: 104.4 MB (104367931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c404b2d39d60e0d725c56d4fa8552e1a9e0e9828b5f3d343f7b7cc1c2495dbd`  
		Last Modified: Thu, 26 Feb 2026 19:24:32 GMT  
		Size: 18.9 KB (18919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de9a10b141d51cc8b7009546021ff5c881345a4095c7b0d2c2461215a58f71c`  
		Last Modified: Thu, 26 Feb 2026 19:24:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16156cb578d453d154abf58881629fcee54d1e21cc3ddae107f211aa236fe19`  
		Last Modified: Thu, 26 Feb 2026 19:24:32 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ecc4d0a517c3bc516b646e342458a0e6e1511b100dc149a394592056ca8b5a`  
		Last Modified: Thu, 26 Feb 2026 19:24:33 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:62cc7b925f7ee5da83343e49c11f4b2ba070370f7dd2a2c3385889705b3c001e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.5 KB (655544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b391446e25e81028a665f7680aa7d9f57fa28cc8b45f2f79b6601bd8c46771`

```dockerfile
```

-	Layers:
	-	`sha256:17132c80b8bc776e82e1008b42ce0f456fa4b4a231f7aed896b1a49a1523288f`  
		Last Modified: Thu, 26 Feb 2026 19:24:30 GMT  
		Size: 615.2 KB (615236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:328dcc7fd9f2bd39b680870630b3c79ad2bcb55dc208b9cfb4663d59f1ede87c`  
		Last Modified: Thu, 26 Feb 2026 19:24:31 GMT  
		Size: 40.3 KB (40308 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:c673fa785ecaed16e5c5a0e35ae04b17a73869dd8922c151151ae21a5e0602e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119830082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3061b05668b98df4d56b785d4edfd45d86ead1b1e061926d989a02f7d5f8b3a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:16:26 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:16:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:16:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:16:29 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:16:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:16:29 GMT
ENV PG_MAJOR=18
# Thu, 26 Feb 2026 19:16:29 GMT
ENV PG_VERSION=18.3
# Thu, 26 Feb 2026 19:16:29 GMT
ENV PG_SHA256=d95663fbbf3a80f81a9d98d895266bdcb74ba274bcc04ef6d76630a72dee016f
# Thu, 26 Feb 2026 19:16:29 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:19:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:19:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:19:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:19:16 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 26 Feb 2026 19:19:16 GMT
VOLUME [/var/lib/postgresql]
# Thu, 26 Feb 2026 19:19:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:19:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:19:16 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:19:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:19:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f900c73cf7d491355f8ccb851c8ca2a2cd6bf5a4528e310a1d428dd0852859ef`  
		Last Modified: Thu, 26 Feb 2026 19:19:31 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaafe8751749cbb48fe9aba2611892ad7eec97371aee19e5458f87b867dc3a5`  
		Last Modified: Thu, 26 Feb 2026 19:19:31 GMT  
		Size: 890.6 KB (890637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cd406e3de77a336a5b66693b0df12ecc114e6fb33f0fd17bbd1961aaff7302`  
		Last Modified: Thu, 26 Feb 2026 19:19:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f095b1a40163e06f7faa2c19de5ab2e705e600b5edd8087b968744355de459c`  
		Last Modified: Thu, 26 Feb 2026 19:19:34 GMT  
		Size: 115.3 MB (115292558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5765e877b5e010cf684dd9f3d0599510bcf691158c3e169703e68ab04286f30e`  
		Last Modified: Thu, 26 Feb 2026 19:19:32 GMT  
		Size: 18.9 KB (18916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29764188c7286d22ce3a6e07cd6ab0e7b399f0f225c7b8843ce6d49d6099d1a7`  
		Last Modified: Thu, 26 Feb 2026 19:19:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f3cba665b3764d275c4334f68ef31f582d42e815c203f6a7c546cc4d4dc5ae`  
		Last Modified: Thu, 26 Feb 2026 19:19:33 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4baafc77f1e0dd428d70526edae822a7bbb236ff8bfb06729c299ad956a1e4`  
		Last Modified: Thu, 26 Feb 2026 19:19:34 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:21cfc58739d7563ad3a1ac98cac9a487ba47b064d623b4c4b0713f106d00ba57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.3 KB (655259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40412da3bcc91ee9855eecab5241d3542f9da5e9e80902b22dc05eea7dbc69a3`

```dockerfile
```

-	Layers:
	-	`sha256:859cdd80c96504e74fbf947c2827b14caa1645e0b0e4df6039cf5dba67a03c6e`  
		Last Modified: Thu, 26 Feb 2026 19:19:32 GMT  
		Size: 615.2 KB (615172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ce74ea865075ceee75331fe707cb5b62bf1ffd5cc4f1447e286b8f16f633259`  
		Last Modified: Thu, 26 Feb 2026 19:19:31 GMT  
		Size: 40.1 KB (40087 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:8ec079d11c5b50fe88ed3b6355fe84004f9d86f8692913fd8d01dda4a0090d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97440021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca97206bd656ae996733ef7731f20ee34c876625fac0c8fb1809e4dcbe28828e`
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
# Thu, 26 Feb 2026 19:16:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:16:11 GMT
ENV PG_MAJOR=18
# Thu, 26 Feb 2026 19:16:11 GMT
ENV PG_VERSION=18.3
# Thu, 26 Feb 2026 19:16:11 GMT
ENV PG_SHA256=d95663fbbf3a80f81a9d98d895266bdcb74ba274bcc04ef6d76630a72dee016f
# Thu, 26 Feb 2026 19:16:11 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:20:10 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:20:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:20:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:20:11 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 26 Feb 2026 19:20:11 GMT
VOLUME [/var/lib/postgresql]
# Thu, 26 Feb 2026 19:20:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:20:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:20:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:20:12 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:20:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:20:12 GMT
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
	-	`sha256:a2dd9140646d1c7adfd00d17e1e8bad6e07c4e46d7ca4cb79325183f1fa7750a`  
		Last Modified: Thu, 26 Feb 2026 19:20:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8602736e187b8941b3cbd12b5b032603f8dc0ec5ba19374ef18f57bc0f5e499f`  
		Last Modified: Thu, 26 Feb 2026 19:20:46 GMT  
		Size: 92.8 MB (92800521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c703d2a0c6f2090bbcbf937d96438e6b328a1a65e81b44dc87a1e0ebd07295`  
		Last Modified: Thu, 26 Feb 2026 19:20:41 GMT  
		Size: 18.9 KB (18924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d91ba94701e855c42c063b0af1bd51595b62d29614d55a69417cb7b7d6b2cec`  
		Last Modified: Thu, 26 Feb 2026 19:20:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40246bf338c15cd24dd17fd64f71c5dd6fa62a3317ea156a19df43726a8643d8`  
		Last Modified: Thu, 26 Feb 2026 19:20:42 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03693c8688cf304a00179136157c7af32fecf6c6386fc858aaa1707c4cbca200`  
		Last Modified: Thu, 26 Feb 2026 19:20:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:5b217ba51c1074d37e0f041cdf50fca9eb3ecf3f48ca0996d9efdbb704f97593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.8 KB (651778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec13569b64c05f3d576e6f16c1ff983d534f5361025c9ffe53ee54733c90a40`

```dockerfile
```

-	Layers:
	-	`sha256:2b293f66b7063bfadccb579e3b78f939e31d5e228be044da2032e9b2128e0aef`  
		Last Modified: Thu, 26 Feb 2026 19:20:41 GMT  
		Size: 611.6 KB (611607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c6d8a7b3f479a0f4235b52d275a7dfb88bea6a908c907d494e0c387ffff7f59`  
		Last Modified: Thu, 26 Feb 2026 19:20:41 GMT  
		Size: 40.2 KB (40171 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:4c8e986018edd29e295c353b760c54807497b77f27427497641623aa23985e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.7 MB (113692733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510173ba89a9868c83adfd0fe24cff0be1593eba549a53c8e18503ebd40469e9`
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
ENV PG_VERSION=18.3
# Fri, 13 Feb 2026 00:03:22 GMT
ENV PG_SHA256=d95663fbbf3a80f81a9d98d895266bdcb74ba274bcc04ef6d76630a72dee016f
# Fri, 13 Feb 2026 00:03:22 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 28 Feb 2026 04:14:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 28 Feb 2026 04:14:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 28 Feb 2026 04:14:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 28 Feb 2026 04:14:57 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Sat, 28 Feb 2026 04:14:57 GMT
VOLUME [/var/lib/postgresql]
# Sat, 28 Feb 2026 04:14:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 04:14:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 28 Feb 2026 04:14:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 04:14:57 GMT
STOPSIGNAL SIGINT
# Sat, 28 Feb 2026 04:14:57 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 28 Feb 2026 04:14:57 GMT
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
	-	`sha256:00eb820348ba9228e1757b2173935230b15e888e2887cbac2b79c7dcd0e7b353`  
		Last Modified: Sat, 28 Feb 2026 04:18:07 GMT  
		Size: 109.3 MB (109282508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f396d65aebd5deac00810cbed6a795a5ebe4ffe8507760fe83e80cf198d1a07`  
		Last Modified: Sat, 28 Feb 2026 04:17:50 GMT  
		Size: 18.9 KB (18926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c251a5322241b38b45401a94c6faf66869ec721bdbace09daa9413bdae6e78ac`  
		Last Modified: Sat, 28 Feb 2026 04:17:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db819da4b3b6787fc026d96237460c90941ae41fa8295930c99fcafc4a60ee74`  
		Last Modified: Sat, 28 Feb 2026 04:17:50 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d38896638d9eb572c3e8c8e5059eca7699f9b85378b50927280f71db9c0c2`  
		Last Modified: Sat, 28 Feb 2026 04:17:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:b6fda7c7213ea3f988269b46f2561d3f03308021d035cde1208144bb3704e9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.4 KB (653440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c5ebe0fc51fe469bcc32363fe72bf77d7cb714a600855fc5f969bc435fb939`

```dockerfile
```

-	Layers:
	-	`sha256:e70840476539520ceb6e195e77539c07d0b228547875e746757ca0e922de6dab`  
		Last Modified: Sat, 28 Feb 2026 04:17:50 GMT  
		Size: 613.3 KB (613265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f350632890880584516614fb25c4c39d7760731ca3f2fa8de53de65aa582b4`  
		Last Modified: Sat, 28 Feb 2026 04:17:50 GMT  
		Size: 40.2 KB (40175 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:eb7d8b9059a1291276ef5a2aac7dd90bc1280a3397138484986a607cd60aec19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122313221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0f8ed2d36f70db7023bd0578d36a6bd3e29014c92835ccd2d1467e90e96f87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:14:50 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:14:56 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:14:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:14:56 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:14:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:14:56 GMT
ENV PG_MAJOR=18
# Thu, 26 Feb 2026 19:14:56 GMT
ENV PG_VERSION=18.3
# Thu, 26 Feb 2026 19:14:56 GMT
ENV PG_SHA256=d95663fbbf3a80f81a9d98d895266bdcb74ba274bcc04ef6d76630a72dee016f
# Thu, 26 Feb 2026 19:14:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:19:04 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:19:04 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:19:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:19:04 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 26 Feb 2026 19:19:04 GMT
VOLUME [/var/lib/postgresql]
# Thu, 26 Feb 2026 19:19:04 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:19:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:19:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:19:05 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:19:05 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:19:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c67cc230b3dd7b560fa1987c9d84e3183b632f12d48ce939c5c92b1ccb3f06`  
		Last Modified: Thu, 26 Feb 2026 19:19:31 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fea80e1df1f3240aa5c657b48535279b84e09b47913351236b888b90c60dcaa`  
		Last Modified: Thu, 26 Feb 2026 19:19:32 GMT  
		Size: 894.4 KB (894422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59f3692ca9d6431e97119057c4dd58ae72f689adbada9d479011f70a5f50279`  
		Last Modified: Thu, 26 Feb 2026 19:19:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047985b5b32c6cd07a44a2dacc386b5c314c5756d8550ec7f490bda70d0a392f`  
		Last Modified: Thu, 26 Feb 2026 19:19:34 GMT  
		Size: 117.7 MB (117742204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46eea623ee29bed8cc837640214e106990b4696216992fd2c49805bf64ad9a93`  
		Last Modified: Thu, 26 Feb 2026 19:19:32 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704cbf1210f8610b92f666d6fac8397a853d88ae0e34830d586d9256fda7d52e`  
		Last Modified: Thu, 26 Feb 2026 19:19:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7aec424f4c597fe0fd5e491df930d523390fe3a156d62e92db75263a14c1ab3`  
		Last Modified: Thu, 26 Feb 2026 19:19:33 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a62f9ddd61956244fae7f998e86e214fadef4a7d11ffc7e7adf983421b97c7`  
		Last Modified: Thu, 26 Feb 2026 19:19:33 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:6bc5822bf6887fe12044a74a5da8d2cfd0eaf39d0d844fd65b3d2aee5ef63199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.4 KB (653367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc64f256dd2b4ebc9cf0c22d03d8e6eb386de4d1f0cf2e2eaf9d749b814120a`

```dockerfile
```

-	Layers:
	-	`sha256:082012b402696f2b9b21f8b41e4fc31a6541b1e021c57d418536e017b934bf51`  
		Last Modified: Thu, 26 Feb 2026 19:19:32 GMT  
		Size: 613.2 KB (613241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e989bbed6dd9447d9d1875b2366b8a04dddfd19513d37ec994dd663f4ed1414f`  
		Last Modified: Thu, 26 Feb 2026 19:19:32 GMT  
		Size: 40.1 KB (40126 bytes)  
		MIME: application/vnd.in-toto+json
