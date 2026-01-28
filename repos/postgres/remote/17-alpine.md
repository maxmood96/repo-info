## `postgres:17-alpine`

```console
$ docker pull postgres@sha256:820d67c4428ef2b8a8644ccba24116268c9f705369484042bec5cba2004cdca7
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
$ docker pull postgres@sha256:a6d31f853205ce20d399df4e33a0b4c715672f232f4ee7440499747e6e02c126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111062762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9104a94e25680111c00d6c9ad5913129d2f45c1bc51b363db177d638c313392e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:29:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:29:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:29:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:29:43 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:29:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:29:43 GMT
ENV PG_MAJOR=17
# Wed, 28 Jan 2026 02:29:43 GMT
ENV PG_VERSION=17.7
# Wed, 28 Jan 2026 02:29:43 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Wed, 28 Jan 2026 02:29:43 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:32:18 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:32:18 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:32:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:32:18 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:32:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:32:18 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:32:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:32:19 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:32:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:32:19 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:32:19 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:32:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b44578fdd0f5ce81354f279b3cd8d78ffca2125de0227ed46689bdb7e67783`  
		Last Modified: Wed, 28 Jan 2026 02:32:35 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a6f84ff1b1fed7e4e64d9a0e7dc2056f6f64165a23ece405fc4ef1861d38f9`  
		Last Modified: Wed, 28 Jan 2026 02:32:35 GMT  
		Size: 922.9 KB (922900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26cc44de3968d043bc283cc8783b225c08484af1afcbbd88309f36ea0a6c01a`  
		Last Modified: Wed, 28 Jan 2026 02:32:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f26294f82c72a1a6403ab7a6f19567eb8a27ca800196fc247e2424ab40a8247`  
		Last Modified: Wed, 28 Jan 2026 02:32:38 GMT  
		Size: 106.3 MB (106260756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972c8196a49da477acbc980eded1bc401314aa0e5a21a1c94459ed2840cfcd19`  
		Last Modified: Wed, 28 Jan 2026 02:32:35 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc0c881ca9f47d0de8b3cb9f13b863fa7cecd59163daf23e4b4677cc1846fc5`  
		Last Modified: Wed, 28 Jan 2026 02:32:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa42ff50bd7552666cfc79a1f63bdff59c974aea268081309a9b9054317ded15`  
		Last Modified: Wed, 28 Jan 2026 02:32:37 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc33a7030518907eae5852a9cf5b70885e979b8744d014f286b51987fe9fcfa`  
		Last Modified: Wed, 28 Jan 2026 02:32:37 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf6e9fd77fde82b6b9f4f914a7f15b6213dee8454a77c10397ff22bd79454f2`  
		Last Modified: Wed, 28 Jan 2026 02:32:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:f2929f58cef6295c9c66632c91be36b6f100e1e7328336de61a1e3775290c759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.8 KB (639752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbd58dba222dbea245136c1c0d4bca4846ae3f65aea5075663c74e90eb4b898`

```dockerfile
```

-	Layers:
	-	`sha256:81b0935ef2bf829ac5f820eb8ab298357432971d6b719f6565ca7b589effa789`  
		Last Modified: Wed, 28 Jan 2026 02:32:35 GMT  
		Size: 598.1 KB (598074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ab572a63f0adf2f8c900424dd071cc4b87c3923c08c02fcdec8a8dba24e2922`  
		Last Modified: Wed, 28 Jan 2026 02:32:35 GMT  
		Size: 41.7 KB (41678 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:97ce46e8cefa26d743a7c3b7cb42860d83ba81ff0ccb7ba1a6232b92ef9a993e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90468845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921d23f69301c741596a7634c79443e8f4bc170c9d690aef33e24ecd71a9a7b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:45:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 00:45:21 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 00:45:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 00:45:21 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 00:45:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 00:45:21 GMT
ENV PG_MAJOR=17
# Thu, 18 Dec 2025 00:45:21 GMT
ENV PG_VERSION=17.7
# Thu, 18 Dec 2025 00:45:21 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Thu, 18 Dec 2025 00:45:21 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 00:48:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 00:48:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 00:48:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 00:48:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Dec 2025 00:48:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Dec 2025 00:48:30 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Dec 2025 00:48:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:48:31 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 00:48:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:48:31 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 00:48:31 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 00:48:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bd087b97c2df2bc0695ce1610fe67c996685fda949d567f03d77be2ffd5ffd`  
		Last Modified: Thu, 18 Dec 2025 00:48:41 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f005fd019e4f85b17fe0e72b86364208eac7042c838f1f9d40f42f5980b30c7`  
		Last Modified: Thu, 18 Dec 2025 00:48:41 GMT  
		Size: 889.5 KB (889473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080689016fbce3f913a7bc32ff0bfa318d2a4668309af8c0d5ed0160315db73c`  
		Last Modified: Thu, 18 Dec 2025 00:48:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d71ba58e80941ac6b0253470f756ffd47ce85058973f851ec347c720c25cea4`  
		Last Modified: Thu, 18 Dec 2025 00:48:43 GMT  
		Size: 86.0 MB (85993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b324223b804737570a63f9ae562b6ccff87f7d9558201b5d0e909d68c974e`  
		Last Modified: Thu, 18 Dec 2025 00:48:42 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7725baa1b9b9fc92b36e663dad070053086f9700ace8bd4fe1d1c6b5296f5ce1`  
		Last Modified: Thu, 18 Dec 2025 00:48:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb08cfe2db3ecb511367e4c831bb88f5ebae629a42cb708f1f280b305827adb`  
		Last Modified: Thu, 18 Dec 2025 00:48:43 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79348ff3646730647b66db81425a41469862e9c1b36cf4220e44abd5cf6066f`  
		Last Modified: Thu, 18 Dec 2025 00:48:43 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564cb2a1f20f7f16fafaae0912ab697ee13673a0316e92f4801876f528983d63`  
		Last Modified: Thu, 18 Dec 2025 00:48:43 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:1962626de48928c67f394f200c847641b52d4c9295dc8339ddf21ec0fb18c7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 KB (41628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32146c31d1a703a694bd7467284d81a0ac1af1de091ad100429fc1ef5147a1b`

```dockerfile
```

-	Layers:
	-	`sha256:8d5a74ccb1feec6a59b158740eafc3774cbe9fd072e2ee24a805ab7bc7c6e27c`  
		Last Modified: Thu, 18 Dec 2025 00:48:41 GMT  
		Size: 41.6 KB (41628 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:82830ba4adbcd7489aa07ca732734d1e0e5ab00466968fe516335a72f6e48959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85666098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9b46bf593a05daf909ea5e2fd8354360d506b606e634c3af9226c8ded31fe9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:44:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:44:45 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:44:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:44:45 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:44:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:44:45 GMT
ENV PG_MAJOR=17
# Wed, 28 Jan 2026 02:44:45 GMT
ENV PG_VERSION=17.7
# Wed, 28 Jan 2026 02:44:45 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Wed, 28 Jan 2026 02:44:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:48:18 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:48:18 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:48:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:48:18 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:48:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:48:18 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:48:19 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:48:19 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:48:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:48:19 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:48:19 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:48:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e6374d99781c40a631331da250474bfec3dbafb2441ad6868df8f6d3f67756`  
		Last Modified: Wed, 28 Jan 2026 02:48:30 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bc1793d210d366bdae402453b2fa0e80dce21060ce8b7302e32c4ace6346b6`  
		Last Modified: Wed, 28 Jan 2026 02:48:30 GMT  
		Size: 889.5 KB (889497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18cee917af91262f31284c2c460b13a12726328984a7ae3577adf04f6469028`  
		Last Modified: Wed, 28 Jan 2026 02:48:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bcc9daa7942c48c57f0cf72a9c4b433409add595945ec7bd8a4b7dfedf12a6`  
		Last Modified: Wed, 28 Jan 2026 02:48:32 GMT  
		Size: 81.5 MB (81477591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9aa2e8cbbdf690bcb6cf52f3f91ebbd5b3a39e9fcd5d124f2b2d4062c4c309`  
		Last Modified: Wed, 28 Jan 2026 02:48:31 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3074d55c42b7e88a5ff4386f2900f6f9d634908a770ff3eefb305e599de9edff`  
		Last Modified: Wed, 28 Jan 2026 02:48:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c554d424cc3e477e51eb363e124854f20abf00f20b93a5ac59c615cdf62f4bf`  
		Last Modified: Wed, 28 Jan 2026 02:48:32 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49314c001f5383f1a4bf62f5aa49d43113081f455ff564c85f2ed66b9c89020e`  
		Last Modified: Wed, 28 Jan 2026 02:48:32 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cea73286bb8db71a233413a854cfdbb89db74798bbf91223580ee7e9b0e88f`  
		Last Modified: Wed, 28 Jan 2026 02:48:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:d480f0e2225a36953d0bc880e7a65a2490e009b28376f57cd30eefc69a12f046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.3 KB (639303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a376bcd7ea888af984598442de42ee1ca9b1b8b18c83c00bf8dd847b0a7999c`

```dockerfile
```

-	Layers:
	-	`sha256:274668d10ebe10a6c6994235b42d4214e4545893e288a07487f2fcc1e4c7e540`  
		Last Modified: Wed, 28 Jan 2026 02:48:30 GMT  
		Size: 597.5 KB (597460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07cce88ea8cb4068743e992fa8027f46202f8f39c0f9f0570cca8fdf7a324a0d`  
		Last Modified: Wed, 28 Jan 2026 02:48:30 GMT  
		Size: 41.8 KB (41843 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:14b9e8eea0d2425bc2e02db4b0a0c5837663891cd1177d2be4df0f704e8d7fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109263881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19d6e56b4b4e3f48b9624e1d3faca9f7bdfd53bb2b990c7f5b021243a4621e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:31:35 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:31:38 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:31:38 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:31:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:31:38 GMT
ENV PG_MAJOR=17
# Wed, 28 Jan 2026 02:31:38 GMT
ENV PG_VERSION=17.7
# Wed, 28 Jan 2026 02:31:38 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Wed, 28 Jan 2026 02:31:38 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:34:00 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:34:00 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:34:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:34:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:34:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:34:00 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:34:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:34:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:34:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:34:01 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:34:01 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:34:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7457159af92bea8a499e24075cb8c228c597d1a4b4b4723408f006d600dc19aa`  
		Last Modified: Wed, 28 Jan 2026 02:34:15 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7688a7195d194b5a041ab39a1e7e5c403495228c34fc932af0ea576b4043459e`  
		Last Modified: Wed, 28 Jan 2026 02:34:15 GMT  
		Size: 876.5 KB (876485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3716bdff25f8ced0f4ee240224bce4a858eafaa9569b6885e9ec6da67c2fb81`  
		Last Modified: Wed, 28 Jan 2026 02:33:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15ab3a99e6db89d052094b078366d142973bd854c507906b060dfca0bb0b476`  
		Last Modified: Wed, 28 Jan 2026 02:34:18 GMT  
		Size: 104.2 MB (104173020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bab95e30c3d5cdc511c26010288d1c6849b1ab2c6f7a23002fb03c959e0a1ea`  
		Last Modified: Wed, 28 Jan 2026 02:34:16 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45fbb8a6b196110030e1e10dbd8fbe2515b373844852f6b1e4d83a302b0368f`  
		Last Modified: Wed, 28 Jan 2026 02:34:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae3a3be54606b19c8cc23013d2bf822e0013fa842413bf548374a81e32a977c`  
		Last Modified: Wed, 28 Jan 2026 02:34:16 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5ffc2fd9c118f5cad255ed82b330599dbb583d8b7e28714779914861645d0b`  
		Last Modified: Wed, 28 Jan 2026 02:34:17 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c17960ea189beea1774edadf59a3d831c554b2c923741df9cf1c8a51c372da5`  
		Last Modified: Wed, 28 Jan 2026 02:34:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:e1fa5d57a33b85455bf805bf49c61a1726351705712034a1d226e1419f348883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.4 KB (639367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebe7493f15773c4ceaba25fec963b5f40631e5688719caa6db639678d3c5106`

```dockerfile
```

-	Layers:
	-	`sha256:d9487c19c879434c2a25ece5f8819dddd210d1d55647d31576774ad588de1f3f`  
		Last Modified: Wed, 28 Jan 2026 02:34:15 GMT  
		Size: 597.5 KB (597480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9233cc3386014da87d65f2e99f42f2a6742580e993476b5236487e24cc2e1933`  
		Last Modified: Wed, 28 Jan 2026 02:34:15 GMT  
		Size: 41.9 KB (41887 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; 386

```console
$ docker pull postgres@sha256:08c6c96d2f889bd04c0952b3c68d61ff457334ba0de875f1f8672294f7951b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117145218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f3506165eb7eb492f52d236983cd73401ad79c1e5c0816dfbbaf05e2381716`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:26:03 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:26:06 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:26:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:26:06 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:26:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:26:06 GMT
ENV PG_MAJOR=17
# Wed, 28 Jan 2026 02:26:06 GMT
ENV PG_VERSION=17.7
# Wed, 28 Jan 2026 02:26:06 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Wed, 28 Jan 2026 02:26:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:28:49 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:28:49 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:28:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:28:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 02:28:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 02:28:49 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 02:28:49 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:28:49 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:28:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:28:49 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:28:49 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:28:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4829aad8e62d21ce4d9b75cdb4ebf9c8e04c6d9782d3e8a691063764cb747357`  
		Last Modified: Wed, 28 Jan 2026 02:29:05 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0d02dea31c5d195eb5061f6eac601a764dd4f02314416b0f4fcc3fe42103e4`  
		Last Modified: Wed, 28 Jan 2026 02:29:05 GMT  
		Size: 893.2 KB (893247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74183b1eb0b64ac7d0c80a3932b88fe48fee3d7b4c9d479ad490b9862e7b2cfb`  
		Last Modified: Wed, 28 Jan 2026 02:29:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a5d93da3e77d3787917dbbe15c7ff4a4fdff6572ba3f4c007786038a5db063`  
		Last Modified: Wed, 28 Jan 2026 02:29:08 GMT  
		Size: 112.5 MB (112547684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608ed10ed6dd8fb5d16607a5ba784e1722a9c3a6d5ed07fbee4f726919516f47`  
		Last Modified: Wed, 28 Jan 2026 02:29:06 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93993c8fa756f3b09c3ad1fe85d1e0a34229d504688cc39fb81cb108ea9c97b`  
		Last Modified: Wed, 28 Jan 2026 02:29:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25040e0b480e1b417973622b2bf1f8a3f2301c9671d4324bbec379e36f904e9f`  
		Last Modified: Wed, 28 Jan 2026 02:29:07 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8828980a5755a9177c06005aea85db9810874a6c9b1bd1ccabab1372e72eda76`  
		Last Modified: Wed, 28 Jan 2026 02:29:07 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222263efb5f389e53d1f46db29c69b8920fc1247ccb6edd11c41f7fbff6ebd26`  
		Last Modified: Wed, 28 Jan 2026 02:29:07 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:28842f2f0c1abdda9fa5dfab99dc7d5e9ffaa40a2519fd39f50b73db7a26ae67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.7 KB (639681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c63da12e1f3aefc04a50eb87cfd280ccfda89ac1fcc69422d17cf7114ce47f2`

```dockerfile
```

-	Layers:
	-	`sha256:579f062cbf5ffc8a130578efda454a4060c09c5d256ec5a653257ccb49f4587e`  
		Last Modified: Wed, 28 Jan 2026 02:29:05 GMT  
		Size: 598.0 KB (598049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f69c26f5fd95944c5cbaa5db1eeb7dbd7cc82d848bf57125c242bd541246ff5`  
		Last Modified: Wed, 28 Jan 2026 02:29:05 GMT  
		Size: 41.6 KB (41632 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:20af0f82de75e3f0f4017d68addadbfe15b54ba16238744c312ace0aad4bacd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96058253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d944a7270ce54db699b690483437ffaa1c139396f60a67decff473ea3a2d70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:31:57 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 03:32:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 03:32:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 03:32:03 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 03:32:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 03:32:03 GMT
ENV PG_MAJOR=17
# Wed, 28 Jan 2026 03:32:03 GMT
ENV PG_VERSION=17.7
# Wed, 28 Jan 2026 03:32:03 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Wed, 28 Jan 2026 03:32:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 03:39:10 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 03:39:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 03:39:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 03:39:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 28 Jan 2026 03:39:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 28 Jan 2026 03:39:12 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 28 Jan 2026 03:39:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:39:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 03:39:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:39:14 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 03:39:14 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 03:39:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd4e647df17c82db9ca398b2f463b9b25ee74420a55b31a9516facb1afa9c46`  
		Last Modified: Wed, 28 Jan 2026 03:35:18 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71de422e36f20b27957805987c70f9baf3d78aeb5185cefb6ba5e8f87a61453`  
		Last Modified: Wed, 28 Jan 2026 03:35:19 GMT  
		Size: 881.5 KB (881539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7649bce93f6f6f2482a38dc7082290155239a95f5f9f1e205d69594e44341386`  
		Last Modified: Wed, 28 Jan 2026 03:35:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dec20f2f34c4280e47761b32b8fcda0330c45ce3de8c89d1ea928ba0aaeea18`  
		Last Modified: Wed, 28 Jan 2026 03:39:45 GMT  
		Size: 91.3 MB (91329777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708599511fc68d7917e5bbb7a498813ae5ec17296e1ac222c0087de40a5d8bfa`  
		Last Modified: Wed, 28 Jan 2026 03:39:43 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8500106f854b1c90e9b467ffb0567fdbfe8159d6a25388bf8153a306f28e564e`  
		Last Modified: Wed, 28 Jan 2026 03:39:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d19fb334a46c6334245c0b3fa20883c7f328ba30b3e1963cb1e49abe597dfe`  
		Last Modified: Wed, 28 Jan 2026 03:39:43 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f2d02cac0c505163c095574f82d54c3d42528a97f643f0394eb16d6bdb4651`  
		Last Modified: Wed, 28 Jan 2026 03:39:44 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6000a135891014bd1606ec4723f1de1aeec1dd144dc3da62294b1c08676017e`  
		Last Modified: Wed, 28 Jan 2026 03:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:b84d8836a6a816e155d88a3f49e5f7ce09c1f554278bff9b1c37fc87c3350749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.5 KB (637525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7960c2a337b0ff9d280134d41648a05597e0d1df37768288b33247a3bc2040`

```dockerfile
```

-	Layers:
	-	`sha256:329af452841e52bfdf6837557a651a9d1356d93f04ff70f315619add2c64e2b2`  
		Last Modified: Wed, 28 Jan 2026 03:39:43 GMT  
		Size: 595.8 KB (595795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86d3e2fde75fae100cdb992c36549d3720de50cbe2684d1c372b38a18a3ae495`  
		Last Modified: Wed, 28 Jan 2026 03:39:43 GMT  
		Size: 41.7 KB (41730 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:7ffc0b6e598e3cd2382b5e632ef970dc2b32be1fd4f12fbba6bd80e77b1aa3fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112207413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c264c758e08aa056afa66cf63015744bee0d3106d015cc7ac00ddc1caeab1a98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 22:58:49 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 22:59:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 22:59:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 22:59:01 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 22:59:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 22:59:01 GMT
ENV PG_MAJOR=17
# Thu, 18 Dec 2025 22:59:01 GMT
ENV PG_VERSION=17.7
# Thu, 18 Dec 2025 22:59:01 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Thu, 18 Dec 2025 22:59:01 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 19 Dec 2025 00:46:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 19 Dec 2025 00:46:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 19 Dec 2025 00:46:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 19 Dec 2025 00:46:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 19 Dec 2025 00:46:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 19 Dec 2025 00:46:58 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 19 Dec 2025 00:46:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 00:46:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 19 Dec 2025 00:46:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Dec 2025 00:46:59 GMT
STOPSIGNAL SIGINT
# Fri, 19 Dec 2025 00:46:59 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 19 Dec 2025 00:46:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e7504fb8b5ca902553810400e8ecf856a5984c36fb7dba7b9d1932f5432750`  
		Last Modified: Thu, 18 Dec 2025 23:52:05 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254154902548782aac7bbe74d12c713d81df39d8b697e905a7ada02053473207`  
		Last Modified: Thu, 18 Dec 2025 23:52:05 GMT  
		Size: 868.9 KB (868948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cb1e707cecbd8b342e8230a81de52b30274d906375bb62c7f6fa905a968ed1`  
		Last Modified: Thu, 18 Dec 2025 23:52:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9987107d28c9e88c7b892f13e8c2fe6751beedb287c6bafe2f7b42d7e26428`  
		Last Modified: Fri, 19 Dec 2025 00:50:07 GMT  
		Size: 107.7 MB (107737229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed74815781b105f180251a287a369444a8a1436ed0c8f99e1fbcd3e31382510`  
		Last Modified: Fri, 19 Dec 2025 00:49:52 GMT  
		Size: 9.9 KB (9886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcc974a20a6aeeea569d2e65fc845506efab2cb099720709feee93dac841188`  
		Last Modified: Fri, 19 Dec 2025 00:49:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2dcef190b4a0599e111222fbfd202b1e0bca74bc59115bba1691f6deca38cc`  
		Last Modified: Fri, 19 Dec 2025 00:49:52 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa608030e6ffeaad175a0a78ae3ab434f06a7c6d84c7a1fca5ad241c7abf6df`  
		Last Modified: Fri, 19 Dec 2025 00:49:53 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3adfcb54f2f75b13a9d9a8a8b9faad8ece68f2659a70b1d5ac513b0a153a9d`  
		Last Modified: Fri, 19 Dec 2025 00:49:53 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:7a86b69070d9ed5891e7a4730123421e2dcee460a0f1937df2b297ccb763c999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.2 KB (639189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8c246d1ef0a671e908b9ea30321defb7e571c03b562101f8be168555d475e2`

```dockerfile
```

-	Layers:
	-	`sha256:070449c9ca16d5f280b1649b115d933cbb24bba2def0b7671fdbceebfa786196`  
		Last Modified: Fri, 19 Dec 2025 00:49:52 GMT  
		Size: 597.5 KB (597453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:755b738d0ba83be8cada6d972abfa923158ddb04249ef84bb89573f8df8c9dae`  
		Last Modified: Fri, 19 Dec 2025 00:49:51 GMT  
		Size: 41.7 KB (41736 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:8ee8c699ec9a78da599d48f30ff59d2d302abdbeb83ba79217f143d45c4fab73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119236051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f05efbbce47005119798b2592ba83659a40f9ebd02bcf86510be17025ed0fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:06:33 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 01:06:36 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 01:06:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 01:06:36 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 01:06:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 01:06:37 GMT
ENV PG_MAJOR=17
# Thu, 18 Dec 2025 01:06:37 GMT
ENV PG_VERSION=17.7
# Thu, 18 Dec 2025 01:06:37 GMT
ENV PG_SHA256=ef9e343302eccd33112f1b2f0247be493cb5768313adeb558b02de8797a2e9b5
# Thu, 18 Dec 2025 01:06:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 01:10:53 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 01:10:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 01:10:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 01:10:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Dec 2025 01:10:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 18 Dec 2025 01:10:56 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Dec 2025 01:10:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:10:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 01:10:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:10:57 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 01:10:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 01:10:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:04 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47640600947e6c2716121eaeecb21eafc3f56109bbf28a6b3637e7e493750c2`  
		Last Modified: Thu, 18 Dec 2025 01:11:27 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72711bc192b3b7fee821ed917f13059104e610eeefe93d04d8ae5148c6065ce3`  
		Last Modified: Thu, 18 Dec 2025 01:11:27 GMT  
		Size: 897.4 KB (897412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe5c7e59c1a8c45c7f4247be7fa6a549397dadb23873a8bdbead7595442837b`  
		Last Modified: Thu, 18 Dec 2025 01:11:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b2e32c24c6d242bb948f0020b38e6cb55b135444421f4b27512a7b7a792828`  
		Last Modified: Thu, 18 Dec 2025 01:11:30 GMT  
		Size: 114.6 MB (114597032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bab46b829e978a94cde386b9efbc721a9c7a3ddd5c53ff73f6cd3099c00b2e`  
		Last Modified: Thu, 18 Dec 2025 01:11:28 GMT  
		Size: 9.9 KB (9887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bc258fd2466c3f71e33613c73090352327e5188a2975b25bf63be5ab030cc0`  
		Last Modified: Thu, 18 Dec 2025 01:11:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa27ea9902cdacd552333cf81ec3c32865f2ee7f3536a4c960b3bf54a4e369f`  
		Last Modified: Thu, 18 Dec 2025 01:11:29 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cf26b16770a2f81d0038d8da1e668db0766622e9b4c757d63ea45ac4e10981`  
		Last Modified: Thu, 18 Dec 2025 01:11:29 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54b17c44364a1e36a699b7325d4b178ddd12546ac6c024fbe6bd56bb6095042`  
		Last Modified: Thu, 18 Dec 2025 01:11:29 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:7fa50f7ee11a8039afb369b14b4adf62293f820e78d8f385e4287ce3fb32fa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.1 KB (639101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f425ca72d5e613673cdabd66d8a67a8b795f592cbe47575b268f1acdd2eb6e96`

```dockerfile
```

-	Layers:
	-	`sha256:543d622d66791d51c2918c7e91a459576642efa128d8b57e8f512db1772e8987`  
		Last Modified: Thu, 18 Dec 2025 01:11:27 GMT  
		Size: 597.4 KB (597423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:748ec4c2b62d05397cb1f9d23c12b201ff2358b11eff3219b3ce52e962cc2cdc`  
		Last Modified: Thu, 18 Dec 2025 01:11:27 GMT  
		Size: 41.7 KB (41678 bytes)  
		MIME: application/vnd.in-toto+json
