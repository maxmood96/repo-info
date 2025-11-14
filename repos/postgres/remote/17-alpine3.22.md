## `postgres:17-alpine3.22`

```console
$ docker pull postgres@sha256:465e9a4c730a4ea32e4560f2f1115a8775443b879b7c78b9591420510fd3a981
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
$ docker pull postgres@sha256:f390e2ff8de5c988a05941e3054c6f4b4b15d534b9bb6ab5cca8e0a811baa2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110611570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18fe898888f63f699672306f58c08c9fb6c33a415c2d360aade700ddf9d9066`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 21:06:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:06:07 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:06:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:06:07 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:06:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:06:07 GMT
ENV PG_MAJOR=17
# Thu, 13 Nov 2025 21:06:07 GMT
ENV PG_VERSION=17.7
# Thu, 13 Nov 2025 21:06:07 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Thu, 13 Nov 2025 21:06:07 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Nov 2025 21:08:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:08:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:08:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:08:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:08:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:08:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Nov 2025 21:08:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 21:08:21 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Nov 2025 21:08:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 21:08:21 GMT
STOPSIGNAL SIGINT
# Thu, 13 Nov 2025 21:08:21 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Nov 2025 21:08:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fae39aee7cf316698187a6ff06c3fb8be4c4ddd74e40cea394130b36f0700b0`  
		Last Modified: Thu, 13 Nov 2025 21:08:46 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a6905405fd5402c7f02b91ed2c84377253fad5559a8806272f34404d713176`  
		Last Modified: Thu, 13 Nov 2025 21:08:46 GMT  
		Size: 918.3 KB (918290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b82d6fbe395eea1bc92a31b2995c9ac995781391480e953fa8ac671f097095`  
		Last Modified: Thu, 13 Nov 2025 21:08:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933bee66207d9650734c0312a6adc0f528672f0abd87154b161ea74b4208fe85`  
		Last Modified: Thu, 13 Nov 2025 21:08:57 GMT  
		Size: 105.9 MB (105873298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6f66d1de887dd1a532472ba36d4a0a85b2ea4cea27d959c0a4fc13b7374d20`  
		Last Modified: Thu, 13 Nov 2025 21:08:46 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7f877ea33bf776b15414fc4cf5900f3c0c2f270327b6f03fe5aa32971c3953`  
		Last Modified: Thu, 13 Nov 2025 21:08:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6bff5d0106e36b69ce3677d829f0a5e8bc2bcba601bdbcfcdeae1416092af6`  
		Last Modified: Thu, 13 Nov 2025 21:08:46 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bd5d2bae5b4c332688cfc1be51c40f4b90ed2ef80f577c9d130eaef5be0400`  
		Last Modified: Thu, 13 Nov 2025 21:08:46 GMT  
		Size: 6.1 KB (6077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fde4f6ada431bc109f4503937795066ebd47562e674a0027a58ddcf99790d1a`  
		Last Modified: Thu, 13 Nov 2025 21:08:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:1663f5294416dd21ade667850fecca9c69eff47bfd496ef836ddff9aec9327a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.6 KB (638609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a747cfb62bb4b36368ebfd6db856158061a8becfce1ade8026096eb67b2f39a7`

```dockerfile
```

-	Layers:
	-	`sha256:dcd446c7167f791a19673960159208ea189828bf39f7cd6cc6d662b77dd9816e`  
		Last Modified: Fri, 14 Nov 2025 00:18:10 GMT  
		Size: 596.9 KB (596931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71f789b6d8caf60e23b175a986514c33b5b1f474714cc887ab77e98b4d7d667f`  
		Last Modified: Fri, 14 Nov 2025 00:18:11 GMT  
		Size: 41.7 KB (41678 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:87f45186efc645aad9cb3c9927b760b1cafc173c3b08fc7898dbad7137ddeec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90130237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1419078fe4a2508fb08983e0c80e0748fc7346b7536a2d9323460e513a2a31c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 21:05:36 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:05:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:05:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:05:40 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:05:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:05:40 GMT
ENV PG_MAJOR=17
# Thu, 13 Nov 2025 21:05:40 GMT
ENV PG_VERSION=17.7
# Thu, 13 Nov 2025 21:05:40 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Thu, 13 Nov 2025 21:05:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Nov 2025 21:08:42 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:08:43 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:08:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:08:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:08:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:08:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Nov 2025 21:08:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 21:08:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Nov 2025 21:08:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 21:08:43 GMT
STOPSIGNAL SIGINT
# Thu, 13 Nov 2025 21:08:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Nov 2025 21:08:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a76883056dcf09cb0ff9be27f7d125b052512205a368c0261e2d7608c40346`  
		Last Modified: Thu, 13 Nov 2025 21:09:02 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf5720aae52fafc9ab319f6b0c5c9ee3d9c083aad68ca0b8445a5c22efdb39e`  
		Last Modified: Thu, 13 Nov 2025 21:09:03 GMT  
		Size: 886.1 KB (886138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371460801772f10a2f7eb6fef6c51be26eb8ae84b01c6ee9133ffd3ee6b26680`  
		Last Modified: Thu, 13 Nov 2025 21:08:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66af7be84e6484f3a936126e9e6a7e1d1e0c79edee08c97e2227cf2288836d20`  
		Last Modified: Thu, 13 Nov 2025 21:09:16 GMT  
		Size: 85.7 MB (85722487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f269a9923a1f8d6563d442fff751abfe5b550beaf0b9a218e82967474ee2f7f5`  
		Last Modified: Thu, 13 Nov 2025 21:09:03 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be645db09379d3df75fd7e169f74af349318452318b7241a76ec6dd401a3d45b`  
		Last Modified: Thu, 13 Nov 2025 21:09:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8909da10f668e289823644418fafc899a33dc686f161747646690260afed7fe`  
		Last Modified: Thu, 13 Nov 2025 21:09:03 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d9e98c681680767953bff66bd08f01ea5ab3a037b751b432b46aea814f6f82`  
		Last Modified: Thu, 13 Nov 2025 21:09:03 GMT  
		Size: 6.1 KB (6078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0521c22c704005d4511f75e76a8a077cd3f418f89a2ec9e07f6e7a34763d4be1`  
		Last Modified: Thu, 13 Nov 2025 21:09:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:e28da82a248e0f8e3990a221c040468baed36135210413c228caba2538dd6634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 KB (41628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f3945e8986d6e0247738c8592a6e65f47f0d20f2956926f47c65211ef1b96b`

```dockerfile
```

-	Layers:
	-	`sha256:937f59b652eb0566cd4e8263f9941133d3aa4e824e6f06f34c9981aa743f7b32`  
		Last Modified: Fri, 14 Nov 2025 00:18:14 GMT  
		Size: 41.6 KB (41628 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:09773a4eaebfc0b2b552947f0c8c8923a2d8a595bb8e538cf77374ef86ba1fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85366681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5ce6fda96e9c33dd6faeecc0b5c6095dc6fb73c0ecac16c16df5de030f74b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 21:04:35 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:04:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:04:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:04:40 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:04:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:04:40 GMT
ENV PG_MAJOR=17
# Thu, 13 Nov 2025 21:04:40 GMT
ENV PG_VERSION=17.7
# Thu, 13 Nov 2025 21:04:40 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Thu, 13 Nov 2025 21:04:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Nov 2025 21:07:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:07:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:07:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:07:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:07:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:07:56 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Nov 2025 21:07:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 21:07:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Nov 2025 21:07:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 21:07:56 GMT
STOPSIGNAL SIGINT
# Thu, 13 Nov 2025 21:07:56 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Nov 2025 21:07:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6579a16f86687e4eb54a85fa8992534eadcfb7e1778de2cbab346ba14b655172`  
		Last Modified: Thu, 13 Nov 2025 21:08:31 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c7798c2bbfec2d9566da97f1a0e4c2bbc85e68b6c3723a5b5bd855815bea8a`  
		Last Modified: Thu, 13 Nov 2025 21:08:31 GMT  
		Size: 886.1 KB (886138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a823f6307ef82b08fb2be05d6cc2955a439f1334c4c22cca9388441c2905bf`  
		Last Modified: Thu, 13 Nov 2025 21:08:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cc77d76f9de69b0bd7125dab6ce7a18fd86f6ab6dfe1e55714a0b4dde22a39`  
		Last Modified: Thu, 13 Nov 2025 21:08:38 GMT  
		Size: 81.2 MB (81241451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0692f115305105f370393c2986f013af756c6a3367c97b71bb17c193c7836d2e`  
		Last Modified: Thu, 13 Nov 2025 21:08:32 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a043090f1efe438d9e8d9cd0c2b93e25814726fc684300eeab33b31202809bfd`  
		Last Modified: Thu, 13 Nov 2025 21:08:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bcbab853c670308119dcd1fd8224c33f24e974ddd6ca659b6a7dc5c9341d37`  
		Last Modified: Thu, 13 Nov 2025 21:08:32 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c983e1acac8bef08862add79ddf2c55a477461fe8080707c2f969e8d65b5fda`  
		Last Modified: Thu, 13 Nov 2025 21:08:32 GMT  
		Size: 6.1 KB (6080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1274f1a11be40de8eafff1c1408e7615a6dfc192aeb8ff56fd0c3c602b3dd10`  
		Last Modified: Thu, 13 Nov 2025 21:08:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:46a750a66a94450815daafcd03b8c3d9cad356f2d623ca7764ee4d3a17ba13bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.8 KB (638810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac47b579eb2bab780dc057c53acc484572bd06f68f98e97ddfee3754f7ae58f0`

```dockerfile
```

-	Layers:
	-	`sha256:5c6db2cd1c735aada35d138bbfefccc6e47b790bf8d5e05622cb88447c4acf61`  
		Last Modified: Fri, 14 Nov 2025 00:18:18 GMT  
		Size: 597.0 KB (596967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b66cc5bcfef802a27806ac129fd481ac10ba8fcdb28957aab2bdcfa926af0be7`  
		Last Modified: Fri, 14 Nov 2025 00:18:19 GMT  
		Size: 41.8 KB (41843 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:453582de4eced1d8ebfc59fd849eeba91cf177daaf2606a92ca53f6f5465da36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106570682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7b594326c5d59c0eb103f938c7959db1334e7306b85bbc77aa18f83bf360de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 21:06:51 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:06:53 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:06:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:06:53 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:06:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:06:54 GMT
ENV PG_MAJOR=17
# Thu, 13 Nov 2025 21:06:54 GMT
ENV PG_VERSION=17.7
# Thu, 13 Nov 2025 21:06:54 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Thu, 13 Nov 2025 21:06:54 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Nov 2025 21:09:35 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:09:35 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:09:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:09:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:09:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:09:36 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Nov 2025 21:09:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 21:09:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Nov 2025 21:09:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 21:09:36 GMT
STOPSIGNAL SIGINT
# Thu, 13 Nov 2025 21:09:36 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Nov 2025 21:09:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b880152e535047cf2f3849486503060e4c78916266e294abf4c2a5137646a0f`  
		Last Modified: Thu, 13 Nov 2025 21:09:59 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304f3b44842edbd861de8786e3f9b8e618bfe804e1df3a059aaa115f4d2d8a91`  
		Last Modified: Thu, 13 Nov 2025 21:09:59 GMT  
		Size: 873.5 KB (873478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbdab736cf785bd8c1abd768ba05d254f5db47ed630601b1a9ac9a3d2535f61`  
		Last Modified: Thu, 13 Nov 2025 21:09:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf388a3894db51b2d700c8b7fed35d851dd4f15abba985b565651695382e5b80`  
		Last Modified: Thu, 13 Nov 2025 21:10:13 GMT  
		Size: 101.5 MB (101541611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4625558043726e8ea86d6bdf9c869dcae50cd7dd5f52518ef391d2f0c969696`  
		Last Modified: Thu, 13 Nov 2025 21:10:00 GMT  
		Size: 9.9 KB (9880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343f5d4c0bd100330e7f31360bec5db84d3d1bb0ff21ac2b1f0215fb8431372a`  
		Last Modified: Thu, 13 Nov 2025 21:10:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8f7b2ebdc7d7f3cdb98fd8299730e3b88c4775eeb12064a72488fd1f37b60c`  
		Last Modified: Thu, 13 Nov 2025 21:10:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f82e52a1ae72545dfae559fbe427ee5ebde4e359069fc8d29bbc1a07ecca5b3`  
		Last Modified: Thu, 13 Nov 2025 21:10:00 GMT  
		Size: 6.1 KB (6078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289f5cb107ec70bb3ab4b4f90c6895f3b0e3082009fdc93fdbc14a385d1ebf8`  
		Last Modified: Thu, 13 Nov 2025 21:10:00 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:63a2eb09c034587e89726916339639f6470d3d6f46098ad1815eb67c402523b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.9 KB (638874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e5a5ed77eb53da4160998b4a28931bd393401651ea6dab3c8eb1ca006cca2c`

```dockerfile
```

-	Layers:
	-	`sha256:9ea59df140d0df121d9c1be8d2373f59dccf0d3374247900a30ad10b3d9e2ae2`  
		Last Modified: Fri, 14 Nov 2025 00:18:23 GMT  
		Size: 597.0 KB (596987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c73c6c7c85b3ffb8830ce9718ec4cc62691a294c3248bbf3985e335f1a535338`  
		Last Modified: Fri, 14 Nov 2025 00:18:23 GMT  
		Size: 41.9 KB (41887 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:ff4197fa7564f7c28fe8fd7a3b63eadda6aa0257e5e076827a643400a5388f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116901714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40fd2fa38abaf41a9a3ddcdfaaefb16e9c315d0adbe268480a1cead65469a96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 21:10:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:10:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:10:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:10:43 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:10:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:10:43 GMT
ENV PG_MAJOR=17
# Thu, 13 Nov 2025 21:10:43 GMT
ENV PG_VERSION=17.7
# Thu, 13 Nov 2025 21:10:43 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Thu, 13 Nov 2025 21:10:43 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Nov 2025 21:13:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:13:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:13:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:13:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:13:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:13:09 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Nov 2025 21:13:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 21:13:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Nov 2025 21:13:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 21:13:09 GMT
STOPSIGNAL SIGINT
# Thu, 13 Nov 2025 21:13:09 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Nov 2025 21:13:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d9392767b3f97fce3f87e63400981b72a42b8eadb1d503c47082b93af92ba1`  
		Last Modified: Thu, 13 Nov 2025 21:13:33 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9eb076db47f1999a9bcab52c77502e3124144fb2864ec550a6669a41ad210d6`  
		Last Modified: Thu, 13 Nov 2025 21:13:33 GMT  
		Size: 890.6 KB (890648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db65b123be489b9e9b8cc6f46f7aa9ad9637724f587eddbe48bb39f51788fcf`  
		Last Modified: Thu, 13 Nov 2025 21:13:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ce23dbca7c7693cf70c5c6f82579e794286a1fc20264b9a2eadf7f2a8fae45`  
		Last Modified: Thu, 13 Nov 2025 21:13:48 GMT  
		Size: 112.4 MB (112374607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b2e5bce279ec44bdc93bcd91e314400d694805c451afa9e345a2a5d4818b52`  
		Last Modified: Thu, 13 Nov 2025 21:13:33 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edc76baaf5fe250ae80648b0e5349c6febc6ed2dab30da3d4b6390a5821cb5f`  
		Last Modified: Thu, 13 Nov 2025 21:13:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d918727ca489d00dd2b0cc1e32ad16587c42c39cfd67bc338344c3b315e6bc`  
		Last Modified: Thu, 13 Nov 2025 21:13:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb90b271eff3238c66cbdfc3d0fb26f6ca5a87ead90a3eefa303194fb30f2b1`  
		Last Modified: Thu, 13 Nov 2025 21:13:33 GMT  
		Size: 6.1 KB (6076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd48ead3e6012319207e2c6e6a12c067cf9dd3a72ae629ef582a4e9d83cd42da`  
		Last Modified: Thu, 13 Nov 2025 21:13:33 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:f35b2735a9ce041ce6180025069ae2a8e6113ded0c0ccd41db1af276713d8433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.5 KB (638538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c1c1fc7a858db0b6e4258351a851a096cae67a3a0160dc0cedde72865633f1`

```dockerfile
```

-	Layers:
	-	`sha256:009eb708c80817ef420433909aae588e03b47e964d398351f3ba827a6d1069bb`  
		Last Modified: Fri, 14 Nov 2025 00:18:27 GMT  
		Size: 596.9 KB (596906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8ed5918980cf22d2836fd1f24ae4443d2f7b77f43459085a78aa5e6aba3f8ad`  
		Last Modified: Fri, 14 Nov 2025 00:18:28 GMT  
		Size: 41.6 KB (41632 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:12210ce314a615010e3a281c76e26c07e5f657e53050998ea9a09895b602bd60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94461911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4482f2fd4610772736d323e66556dc8d0760c35dc8a8fa628ddea907e5da5d58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 13 Nov 2025 21:08:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:08:47 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:08:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:08:47 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:08:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:08:48 GMT
ENV PG_MAJOR=17
# Thu, 13 Nov 2025 21:08:48 GMT
ENV PG_VERSION=17.7
# Thu, 13 Nov 2025 21:08:48 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Thu, 13 Nov 2025 21:08:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Nov 2025 21:22:18 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:22:19 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:22:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:22:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:22:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:22:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Nov 2025 21:22:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 21:22:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Nov 2025 21:22:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 21:22:20 GMT
STOPSIGNAL SIGINT
# Thu, 13 Nov 2025 21:22:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Nov 2025 21:22:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d1c66900cf5c9e7948109598cbb47be0e8fe1ad48b504966e9f3463570cfe1`  
		Last Modified: Thu, 13 Nov 2025 21:12:21 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab349f0bd809fd81036764b04799e3daf5f5b6a3591cc2e794e8c13ea16dec`  
		Last Modified: Thu, 13 Nov 2025 21:12:21 GMT  
		Size: 879.0 KB (879032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c1c42c9dff88c0650506b97e1cc305b15e4d760dcf73fd2e765885d7d26ebd`  
		Last Modified: Thu, 13 Nov 2025 21:12:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde2a2aae351ffbcf995631c079c0b97ded2f7c3661002ac08134cdddae2335d`  
		Last Modified: Thu, 13 Nov 2025 21:23:10 GMT  
		Size: 89.8 MB (89833103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867e45e5d5552b85adc59ef02d327485fe82c6e27b8de34d00850b7527ee2b55`  
		Last Modified: Thu, 13 Nov 2025 21:23:04 GMT  
		Size: 9.9 KB (9887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0627fc51dcc9c0ece8fc0c5c8bf6ac3711ddcdcee9e0813db7736d198baabc`  
		Last Modified: Thu, 13 Nov 2025 21:23:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f8d7fc1e5c0a3b9a07885988d69056af9b83e638663e5543da0f72813e68a7`  
		Last Modified: Thu, 13 Nov 2025 21:23:03 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8174af700cd3aab9be1ecdccd72273c4fdfc325ecc4e6bba231b39a48e1731e8`  
		Last Modified: Thu, 13 Nov 2025 21:23:03 GMT  
		Size: 6.1 KB (6078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11544d870b17b562ede630688d1541015937b96a83051939a1171be4f8be9267`  
		Last Modified: Thu, 13 Nov 2025 21:23:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:52da69358e2785906d626111bab1f4b88dc9b7248d3eff44d0f026672241f169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.1 KB (635082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005144fdf6dc1ccf99c1eaa37551cb70f043ff9def3f3a7e0d397292e04cabfd`

```dockerfile
```

-	Layers:
	-	`sha256:ba90bf7855c14e798e93d7dab7e89a98cbefb02a52095cd0193aa7a020a104c2`  
		Last Modified: Fri, 14 Nov 2025 00:18:32 GMT  
		Size: 593.4 KB (593352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7089b2316396a48f12740938fa0de740cfd7f967595abec7ff1f8682c0f603e0`  
		Last Modified: Fri, 14 Nov 2025 00:18:33 GMT  
		Size: 41.7 KB (41730 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:78394367e75092b986f9b979084e8aa36df5a8555860fae94d7edf71751cf532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110677432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1f3627642946b85234777308e93fdebe14c68ad7e1728460b69da985fe8ea1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV LANG=en_US.utf8
# Wed, 15 Oct 2025 18:23:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_MAJOR=17
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_VERSION=17.6
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Wed, 15 Oct 2025 18:23:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Oct 2025 18:23:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 15 Oct 2025 18:23:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Oct 2025 18:23:03 GMT
STOPSIGNAL SIGINT
# Wed, 15 Oct 2025 18:23:03 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Oct 2025 18:23:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84833d3fc2e2327713a740e826ce77ffeb7187fea41b0ab5ee6e3bed55727a29`  
		Last Modified: Fri, 10 Oct 2025 08:00:05 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f9f93d0260214bab91e232f59b30657fb80c4bae9afbda946a88f72abe1f8c`  
		Last Modified: Fri, 10 Oct 2025 08:00:02 GMT  
		Size: 866.6 KB (866623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7890bf4dfc6e8bf86ac7e1227a5c94d034d0b555885f42f439c9506ddeb304`  
		Last Modified: Fri, 24 Oct 2025 08:45:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a7ec81a323c97174d81f16258c78bd917430e13f33c9f5c1ef26e01c782d37`  
		Last Modified: Fri, 24 Oct 2025 11:09:47 GMT  
		Size: 106.3 MB (106278026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfbe10412c13031ca2e736a6532aee9f691292c029f206ce2a53ee4015a064a`  
		Last Modified: Fri, 24 Oct 2025 11:09:38 GMT  
		Size: 9.9 KB (9888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dce7a9fd776fa7b7db8be6bf0a10cbb9dcba64ddf5eb768142cb98b72da868a`  
		Last Modified: Fri, 24 Oct 2025 11:09:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4b1ba2a4a4bda26866dacd6e907b503bc319184500d85f36f794a60ab4c0f`  
		Last Modified: Fri, 24 Oct 2025 11:09:38 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86d1694086626567f91c94397bc999d9a2ce32de01ec27c25e82ad01049ebe1`  
		Last Modified: Fri, 24 Oct 2025 11:09:38 GMT  
		Size: 6.1 KB (6083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777e2fdc1a6e7b3a9cda69388992b092df8f8ab39acc435dca50bdbfce248fe`  
		Last Modified: Fri, 24 Oct 2025 11:09:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:93f460abb0dda82ad2d57b0aa57224db3e352081fe8fe0678d83eefadd951223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.8 KB (636788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f174736bc34584cfc22458137f8dee06022395ffbc08d383592068e18228e9`

```dockerfile
```

-	Layers:
	-	`sha256:3c1c96462ec325074463126633752587d4fd6737572763fd48bead5a23f65a3a`  
		Last Modified: Fri, 24 Oct 2025 14:09:08 GMT  
		Size: 595.0 KB (595010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ded7d74ff3ffb1a49d6c5946c8c6558d4aff55c69a9f44dccc3e3952a6770cf7`  
		Last Modified: Fri, 24 Oct 2025 14:09:08 GMT  
		Size: 41.8 KB (41778 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:0ffddc62f8bdb9381bd99ff92fc930e3fbef0dcf9f43ed16f226394518e55647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119336092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f1d3f3db963119905aa6a711e7b0a02065b4070d17425c93d32a6c1453c741`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 14 Nov 2025 01:06:35 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 01:06:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 01:06:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 01:06:40 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 01:06:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 01:06:40 GMT
ENV PG_MAJOR=17
# Fri, 14 Nov 2025 01:06:40 GMT
ENV PG_VERSION=17.7
# Fri, 14 Nov 2025 01:06:40 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Fri, 14 Nov 2025 01:06:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 14 Nov 2025 01:23:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 14 Nov 2025 01:23:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 01:23:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 01:23:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 01:23:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 01:23:09 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 01:23:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 01:23:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 01:23:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 01:23:10 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 01:23:10 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 01:23:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a6abf741ceaa488adef78c6fd4718d427ce9faca4f7e762b802eaf4bdec87a`  
		Last Modified: Fri, 14 Nov 2025 01:10:10 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcefda53fbfc8d8fdaf00e5371d0e515f34c9bda5a60faabee14e7d74229df72`  
		Last Modified: Fri, 14 Nov 2025 01:10:11 GMT  
		Size: 894.4 KB (894417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c446ed12b3f414acb1aafe9900522337fb7562e6db7b05114b650806a05de80d`  
		Last Modified: Fri, 14 Nov 2025 01:10:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de855e68a69d9d843a2751979977c1917218579c88fde9127fefcd2895a1cb95`  
		Last Modified: Fri, 14 Nov 2025 01:23:50 GMT  
		Size: 114.8 MB (114774907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a33fa7263722c81674631b7f3567ecc75f2d9657f53ded170093d1b2be1c2`  
		Last Modified: Fri, 14 Nov 2025 01:23:40 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62586ebbb7ae79163a789217cb6c3cb75a70bd0560621c4b33d05e663a4ee68f`  
		Last Modified: Fri, 14 Nov 2025 01:23:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186c8a30266663dee1536adc2001dcb63b13d9bbfc71a0b58395e4de7a30d31d`  
		Last Modified: Fri, 14 Nov 2025 01:23:39 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3067f78b2b74d308502bd9e585c7d9dfe8e2c905215b57626f513e7364691902`  
		Last Modified: Fri, 14 Nov 2025 01:23:40 GMT  
		Size: 6.1 KB (6078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a449fb50f3d1cb454257aa087b9037526dcaca8562fc13753b91cafa8c17b967`  
		Last Modified: Fri, 14 Nov 2025 01:23:40 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:ad8cc29705ea39b620f24f16de882dbc332576d59c15d1868da9ac24e960b39b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.7 KB (636658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64d3d78cd7c621d638780fd89a428cf79fe549acde089dd5abf3f080b11dae3`

```dockerfile
```

-	Layers:
	-	`sha256:c4a7f1e7907fabe3ff5c5304d64e347bc6ae14ef17cd675aea0313230fdfcab6`  
		Last Modified: Fri, 14 Nov 2025 03:09:49 GMT  
		Size: 595.0 KB (594980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b61f4f9b5f495040b0ae6afa7ed75776092029f030fb1e709dc46851b6e9cb2`  
		Last Modified: Fri, 14 Nov 2025 03:09:50 GMT  
		Size: 41.7 KB (41678 bytes)  
		MIME: application/vnd.in-toto+json
