## `postgres:alpine3.23`

```console
$ docker pull postgres@sha256:169a12515b04a483f4d508e9f8256edcda9e81409a03f89d6a0461ea59c673f9
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

### `postgres:alpine3.23` - linux; amd64

```console
$ docker pull postgres@sha256:67e0ac5b91c66499110d08892ff16a5b07ea44aa5b5107fba8c996de91f24925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119471878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f7f12398cf7ff3ec5766862ed6770c704fdd466ccf647df7199377e4d18be2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:50:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 19:50:16 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 19:50:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 19:50:16 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 19:50:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 19:50:16 GMT
ENV PG_MAJOR=18
# Mon, 22 Jun 2026 19:50:16 GMT
ENV PG_VERSION=18.4
# Mon, 22 Jun 2026 19:50:16 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Mon, 22 Jun 2026 19:50:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 19:52:50 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 19:52:50 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 19:52:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 19:52:50 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 22 Jun 2026 19:52:50 GMT
VOLUME [/var/lib/postgresql]
# Mon, 22 Jun 2026 19:52:50 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:52:50 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 19:52:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:52:50 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 19:52:50 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 19:52:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b98d99ea642041f9c3c392be0d76a37e222b38499352b1349c5faa405742d11`  
		Last Modified: Mon, 22 Jun 2026 19:53:07 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378f549d73f24a55e1ea0575099468c4a7e020b3a9bf4c60fa95cff0763f4edd`  
		Last Modified: Mon, 22 Jun 2026 19:53:07 GMT  
		Size: 900.3 KB (900262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d192c184925b0f8770daf881157da2c9847a9e2b4d1343325bc2c9e5624a89`  
		Last Modified: Mon, 22 Jun 2026 19:53:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163c40985b517e9fcbdbcb7d7cf32445b3e8c2896477b47f622dcf1b6465af23`  
		Last Modified: Mon, 22 Jun 2026 19:53:10 GMT  
		Size: 114.7 MB (114700780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0214eaec80f9a8ffaeace650f09d403541bb042a24bcf60a63b9d90427fa71e0`  
		Last Modified: Mon, 22 Jun 2026 19:53:09 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759c8e633c403feea428cba6feb1622a70133e1e292788c24d17cb54b0ec8e95`  
		Last Modified: Mon, 22 Jun 2026 19:53:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e266022963f03bf43edfa7545c7467c4e3731bd2458e3af06e5790bb4ba56a74`  
		Last Modified: Mon, 22 Jun 2026 19:53:09 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cc1ea3edbe8e6bc6e16f749adb218f4b961239b17f691ec4578ef88594c9b9`  
		Last Modified: Mon, 22 Jun 2026 19:53:10 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:2fea040dd40c5ce48337ffa8a85eda2667ad9627671b708f0b13b176ccf672e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.5 KB (656508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad68fcf86912d81dbfddbbf962c49fa25bbef77de1c586b393b8ad2feb86d66f`

```dockerfile
```

-	Layers:
	-	`sha256:a987bbf68d60aa5e764a9110f9d8656bc73e2fbcf0e5bf75fe6f55b7e662624f`  
		Last Modified: Mon, 22 Jun 2026 19:53:07 GMT  
		Size: 616.4 KB (616382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4177090f1e6bb3182272e8033e9112342d10ce32f70418f435da5015b233923`  
		Last Modified: Mon, 22 Jun 2026 19:53:07 GMT  
		Size: 40.1 KB (40126 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.23` - linux; arm variant v6

```console
$ docker pull postgres@sha256:4b87c05d5ed61fdfce08f5bd5ddb46a55812ea4a1edc4cf0d32239f5ef24ed1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115652447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e2ab13e82d6d94373a4014183c403e29d72f67e1649b2f8a776afa404742df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:49:43 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 19:49:46 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 19:49:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 19:49:46 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 19:49:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 19:49:46 GMT
ENV PG_MAJOR=18
# Mon, 22 Jun 2026 19:49:46 GMT
ENV PG_VERSION=18.4
# Mon, 22 Jun 2026 19:49:46 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Mon, 22 Jun 2026 19:49:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 19:54:33 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 19:54:33 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 19:54:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 19:54:33 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 22 Jun 2026 19:54:33 GMT
VOLUME [/var/lib/postgresql]
# Mon, 22 Jun 2026 19:54:33 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:54:33 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 19:54:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:54:33 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 19:54:33 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 19:54:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e050c8f29fc32896367d3849c0cbd24c0bfb63582b2938ae9afc156a1f493f4`  
		Last Modified: Mon, 22 Jun 2026 19:54:46 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31b634dcaee4d2ee9ae3c387bff39c958ed3bbd22f157f373df876ff0e924ce`  
		Last Modified: Mon, 22 Jun 2026 19:54:46 GMT  
		Size: 864.6 KB (864630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e71db763f324f1b014ae4d968de1c554bd9df8f3669c99b664d95dc34857b38`  
		Last Modified: Mon, 22 Jun 2026 19:54:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5795e4b3338ba572d6bd84a96eac591c9e843412c8f03310e8d3e0b767aaa541`  
		Last Modified: Mon, 22 Jun 2026 19:54:49 GMT  
		Size: 111.2 MB (111208811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9962c6fa8aa7b7c1997a4c7ad82d2c6d27912016569e854baf291188e6e47a`  
		Last Modified: Mon, 22 Jun 2026 19:54:47 GMT  
		Size: 18.9 KB (18919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03213c3c110d67ddc41653eb21791d4aa750570af0c10f6e04af4d8bbe567c40`  
		Last Modified: Mon, 22 Jun 2026 19:54:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93092b8adb234d8f71e786a4919814c9ae0f86961ef334b917699e2f0665b9bb`  
		Last Modified: Mon, 22 Jun 2026 19:54:47 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68caaaae3a5cb1ef33120db3ed946ab006118f2cc459d663d5a4cb9372ff4f2c`  
		Last Modified: Mon, 22 Jun 2026 19:54:48 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:31156bb6ae8932febd1b7cefd70d1123d216f6a8c72bb3f653a7bbc37635f9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d016cf91b5ad72d4f34d554fd39bbb9044ffc7724617e3635d7431f81e5311`

```dockerfile
```

-	Layers:
	-	`sha256:16797743d3db441b7579d846ea50e4deeae372563243910efe71b08630667615`  
		Last Modified: Mon, 22 Jun 2026 19:54:46 GMT  
		Size: 40.1 KB (40061 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.23` - linux; arm variant v7

```console
$ docker pull postgres@sha256:ef04e894cd0ad4961cf05032da0f2fd4189da84c185a898b224ac72c277db7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109212415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e796c11018f46391e254ac0f99a09d4a9e75525f96d80800192f6a2224d28d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:05:33 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 20:05:36 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 20:05:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 20:05:36 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 20:05:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 20:05:37 GMT
ENV PG_MAJOR=18
# Mon, 22 Jun 2026 20:05:37 GMT
ENV PG_VERSION=18.4
# Mon, 22 Jun 2026 20:05:37 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Mon, 22 Jun 2026 20:05:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 20:08:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 20:08:18 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 20:08:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 20:08:18 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 22 Jun 2026 20:08:18 GMT
VOLUME [/var/lib/postgresql]
# Mon, 22 Jun 2026 20:08:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:08:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 20:08:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:08:18 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 20:08:18 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 20:08:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebc181a7711454437cd387a5d4b81e7843220512a7d59302321aedb862fd075`  
		Last Modified: Mon, 22 Jun 2026 20:08:31 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bf975a69350f0e7c3d33e2180d8f1994bf83c28cd130a1cb64a8d2b146b358`  
		Last Modified: Mon, 22 Jun 2026 20:08:32 GMT  
		Size: 864.6 KB (864639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c82a8759833f27ebb6940b285a6e0714f831608994667c75d665e8f98b7759e`  
		Last Modified: Mon, 22 Jun 2026 20:08:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc06d648fc71be44433420e4bf3f019a19a4cd2285dce720aabe9c6fc34c1138`  
		Last Modified: Mon, 22 Jun 2026 20:08:35 GMT  
		Size: 105.1 MB (105059503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25281d3793ba8ea28a64c52b1804746de6c2df09e4a965fe79c67b0def92edd`  
		Last Modified: Mon, 22 Jun 2026 20:08:33 GMT  
		Size: 18.9 KB (18919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7694a1149aeae1553535d55a058dbeac06886b5d437539807dd564dfad14c52`  
		Last Modified: Mon, 22 Jun 2026 20:08:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dc33a8c5dd3d9b5ad640e042cd19c27eb6ef7a7c8cc88e75d2bd218c7ed6d7`  
		Last Modified: Mon, 22 Jun 2026 20:08:33 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cb4068e866d3c63fa50b356488b5c0bc1bafa580b2d1ba45c70de6f7ac3aa7`  
		Last Modified: Mon, 22 Jun 2026 20:08:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:b9290bf2a9df17960570d199f77ebb9974adc023bfc54cad99d790fc78a0a368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.0 KB (656036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e85d6273fc5c89b19216b2b24874152f391489b28913f85a730aaa5ff903ed`

```dockerfile
```

-	Layers:
	-	`sha256:30e696d900ee6b8cd7e08f84a5bf0568176bb852089fb4dfbf0b80d7d4126775`  
		Last Modified: Mon, 22 Jun 2026 20:08:31 GMT  
		Size: 615.8 KB (615760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d59e5ac54ae22f40cec7afa1c34ace0af15f13293713218ddbe120f0740e2ed9`  
		Last Modified: Mon, 22 Jun 2026 20:08:31 GMT  
		Size: 40.3 KB (40276 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:f0ae663d4d6f6c854ed68b1753da0354fecff475a88e111cf6aadd85bcea09ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117303016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8cc031f7b632941f98f6d225afc954f16e2ace39338f9f9fdcde13eea49fac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:51:02 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 19:51:05 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 19:51:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 19:51:05 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 19:51:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 19:51:05 GMT
ENV PG_MAJOR=18
# Mon, 22 Jun 2026 19:51:05 GMT
ENV PG_VERSION=18.4
# Mon, 22 Jun 2026 19:51:05 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Mon, 22 Jun 2026 19:51:05 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 19:53:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 19:53:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 19:53:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 19:53:25 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 22 Jun 2026 19:53:25 GMT
VOLUME [/var/lib/postgresql]
# Mon, 22 Jun 2026 19:53:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:53:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 19:53:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:53:25 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 19:53:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 19:53:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9815ae4bb0cb5bb67f09607d0506811c8d4291592f5c945de4e2631d0f1cbaa`  
		Last Modified: Mon, 22 Jun 2026 19:53:41 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e60d72789000e0ccc28d6cd6bf9346e20fd2f3499894fa455035ca703b99e0`  
		Last Modified: Mon, 22 Jun 2026 19:53:41 GMT  
		Size: 852.3 KB (852281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29cac74e6538dfdffa1690bfcc22b3a17bd3e07a396e309d1e400e8a916c6f0`  
		Last Modified: Mon, 22 Jun 2026 19:53:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899619521c80d3b37d52f3edd02f00390980263802e8dbe2014abe5de8bc7142`  
		Last Modified: Mon, 22 Jun 2026 19:53:44 GMT  
		Size: 112.2 MB (112242462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1edd6d174ae5c6f41ca533fd95779a1e6d22493f02d04f7e8271a61c011858`  
		Last Modified: Mon, 22 Jun 2026 19:53:42 GMT  
		Size: 18.9 KB (18919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462cb6cf295248d922bafe8fb353b895fbebe354111de0d961f8048380d37609`  
		Last Modified: Mon, 22 Jun 2026 19:53:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d257985b4f84f5eac5db990ab8f94d41526ce8423c4c4cad547ddeed0fda547`  
		Last Modified: Mon, 22 Jun 2026 19:53:43 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1431674b4b23a70c2bcad1b2dc550fe75477bf8b16971d5435e0c99c9f2ea2a0`  
		Last Modified: Mon, 22 Jun 2026 19:53:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:2c41199a238e94098dcfca6c7408d2d7283aa858ca3e681f3222afa490de7a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.1 KB (656084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8685a21a47d2a50bdb2f4cab2ddb6101204444d141d5267d0be022e2e0ba735`

```dockerfile
```

-	Layers:
	-	`sha256:8c9a09f6bf8f99daaefb772b36c4cec345461efd440153de095db779e99d4ab8`  
		Last Modified: Mon, 22 Jun 2026 19:53:41 GMT  
		Size: 615.8 KB (615776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ba1a73932b379fe79e5abfa5de5f5e80732dc77aad2be34b41a6f9426261502`  
		Last Modified: Mon, 22 Jun 2026 19:53:41 GMT  
		Size: 40.3 KB (40308 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.23` - linux; 386

```console
$ docker pull postgres@sha256:6ae038add203ffd3e33c20dfff45f6d714afa194facbf0f533b9204cb63cc5ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126272108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fe4421d91bf5c1d394e8fa4955b7f21110df927b2456dde46e4a2f60e40a16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:50:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 19:50:19 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 19:50:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 19:50:19 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 19:50:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 19:50:19 GMT
ENV PG_MAJOR=18
# Mon, 22 Jun 2026 19:50:19 GMT
ENV PG_VERSION=18.4
# Mon, 22 Jun 2026 19:50:19 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Mon, 22 Jun 2026 19:50:19 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 19:53:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 19:53:31 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 19:53:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 19:53:31 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 22 Jun 2026 19:53:31 GMT
VOLUME [/var/lib/postgresql]
# Mon, 22 Jun 2026 19:53:31 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:53:31 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 19:53:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:53:31 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 19:53:31 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 19:53:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b275b084e565fb7e77b6d7067549a5c61c5d8daef12c4ae320e08a55b618b4`  
		Last Modified: Mon, 22 Jun 2026 19:53:48 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d034f6b553b69d55e26403aec99ac92b6c010d893e8c5334c3e72c7e976ee1b8`  
		Last Modified: Mon, 22 Jun 2026 19:53:48 GMT  
		Size: 868.5 KB (868454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c335c67a4454bdca73f367fc3ec16fc2e1bd3bd622b21e58c30509aca2e99f98`  
		Last Modified: Mon, 22 Jun 2026 19:53:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe81e46671cca95580bc55b30d82be9815174bd17e307ae9807a72a0908bd29`  
		Last Modified: Mon, 22 Jun 2026 19:53:51 GMT  
		Size: 121.7 MB (121709245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d1941dea2c3e2132cd6c0ba5e76e39a34845d3beca4d1aa2966508ba8810fe`  
		Last Modified: Mon, 22 Jun 2026 19:53:49 GMT  
		Size: 18.9 KB (18922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bd40fbf4203f4d4a8e2083624e62644abd051ac61a834009ae237ff2250b65`  
		Last Modified: Mon, 22 Jun 2026 19:53:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e0faec7ef94efa662e26bd9b30b517fb66e4e3ec316005ad695b52f9c43c07`  
		Last Modified: Mon, 22 Jun 2026 19:53:49 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03312683fc3b8af2017b83a7495988b5dbdc254f49f59bc9d27f74d396eb0a0f`  
		Last Modified: Mon, 22 Jun 2026 19:53:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:bd39cea05dec4ee86cd49f9e336214385cc2589596eb03909aba084f6dfe9ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.4 KB (656449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fff196edba21e61ade0be87be0805c2c5d4c8d7121b1a2e63b1a083259a438b`

```dockerfile
```

-	Layers:
	-	`sha256:8d81a3b0f245bc09f30e37638eece0175a59a31eea2faba8320d4979e4b607ad`  
		Last Modified: Mon, 22 Jun 2026 19:53:48 GMT  
		Size: 616.4 KB (616362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a2eb9d877d2ceedbdde99383687f19d0a6fb7a1c8b690018cd1b6f5aa571bcc`  
		Last Modified: Mon, 22 Jun 2026 19:53:48 GMT  
		Size: 40.1 KB (40087 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.23` - linux; ppc64le

```console
$ docker pull postgres@sha256:badc6a7fcbcabfc9ec90b857d592dfeab444adae71042262d84bfc717a1ceb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122431118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef2965e03671fb9338ac00161c2d3d35a2540a17ef85de73177ba2956654ed7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:30:50 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 20:30:54 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 20:30:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 20:30:54 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 20:30:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 20:30:54 GMT
ENV PG_MAJOR=18
# Mon, 22 Jun 2026 20:30:54 GMT
ENV PG_VERSION=18.4
# Mon, 22 Jun 2026 20:30:54 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Mon, 22 Jun 2026 20:30:54 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 20:35:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 20:35:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 20:35:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 20:35:09 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 22 Jun 2026 20:35:09 GMT
VOLUME [/var/lib/postgresql]
# Mon, 22 Jun 2026 20:35:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:35:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 20:35:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:35:10 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 20:35:10 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 20:35:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e9391c05f944b123f5876a64f7d6915dbe05ee717e4f8f20d4c90a5650ddc2`  
		Last Modified: Mon, 22 Jun 2026 20:35:46 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9021869c82cf45db60d7f76a103a86eaa728469afacae3a8f0f41b2c0cf875ae`  
		Last Modified: Mon, 22 Jun 2026 20:35:47 GMT  
		Size: 857.5 KB (857475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e19e3f2b0ba329e63615d8f07287f19cf9e9c0236b3203ea893cb123230a09`  
		Last Modified: Mon, 22 Jun 2026 20:35:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f759e6c67db61d3a2928cb4d3adcb9f6a928f8481d6b2ae460d6bc02af9a4e`  
		Last Modified: Mon, 22 Jun 2026 20:35:52 GMT  
		Size: 117.7 MB (117734925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6ac282d340a740a4c9297342076f409acf913a6434b0604f1ea1be3c1b319d`  
		Last Modified: Mon, 22 Jun 2026 20:35:49 GMT  
		Size: 18.9 KB (18922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f20e9b6d0d01b79941faf06e6759837cfadff7452a596f5bba0734593c1cf0`  
		Last Modified: Mon, 22 Jun 2026 20:35:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94a1126a604a4c78872dfbf48d64a94fb06681fbb8dfea090e14fb9c429186b`  
		Last Modified: Mon, 22 Jun 2026 20:35:49 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd1cbeac8914210a24e69f9d7ce4a6f9096c4bfb30538399cc4f77241ffc4b8`  
		Last Modified: Mon, 22 Jun 2026 20:35:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:add45ec5df164e48f3c81daa9d6099020de3c57ebb6d2a1bc01f97ccbfcad2bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.3 KB (654272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df07f6bbaf501f83beb53bb5a79120ed4f2a870eff34dbbc9bcd1c0019e02d04`

```dockerfile
```

-	Layers:
	-	`sha256:5dd01687c45414225e0b909e1d8cd9f45f4e0f3a959bd1e051f64974f60770cc`  
		Last Modified: Mon, 22 Jun 2026 20:35:49 GMT  
		Size: 614.1 KB (614097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c24ad01547c0c36a0e625510707c9565fc6959724d9536a5e23b1c72e5577448`  
		Last Modified: Mon, 22 Jun 2026 20:35:49 GMT  
		Size: 40.2 KB (40175 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.23` - linux; riscv64

```console
$ docker pull postgres@sha256:af2a5d3db09efa5555e1ed3f0b73fd0151f031652307ee756b1e3b08c40c29bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124117900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a38cfa18b269f4458812886f30c33b62ef7368e3ffdc0575475f0b19f3fde51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 17 Jun 2026 21:19:07 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 17 Jun 2026 21:19:18 GMT
ENV GOSU_VERSION=1.19
# Wed, 17 Jun 2026 21:19:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 17 Jun 2026 21:19:18 GMT
ENV LANG=en_US.utf8
# Wed, 17 Jun 2026 21:19:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 17 Jun 2026 21:19:19 GMT
ENV PG_MAJOR=18
# Wed, 17 Jun 2026 21:19:19 GMT
ENV PG_VERSION=18.4
# Wed, 17 Jun 2026 21:19:19 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Wed, 17 Jun 2026 21:19:19 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Thu, 18 Jun 2026 00:03:19 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Jun 2026 00:03:19 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Jun 2026 00:03:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Jun 2026 00:03:20 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 18 Jun 2026 00:03:20 GMT
VOLUME [/var/lib/postgresql]
# Thu, 18 Jun 2026 00:03:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Jun 2026 00:03:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Jun 2026 00:03:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jun 2026 00:03:20 GMT
STOPSIGNAL SIGINT
# Thu, 18 Jun 2026 00:03:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Jun 2026 00:03:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65f72f9dc4191057d4290d81d3e9b85a1e898cd4566300956d6f215da3e5d2b`  
		Last Modified: Wed, 17 Jun 2026 22:15:32 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfbfbc6e54c945a01fa3a875eb6f9cecc112c80d1bfc687accbcd8cac7b9050`  
		Last Modified: Wed, 17 Jun 2026 22:15:31 GMT  
		Size: 867.5 KB (867539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab6f95812a5a3ce33b21e4c648495817997b01d0e1c0e1bd07538f3f721ede0`  
		Last Modified: Wed, 17 Jun 2026 22:15:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09766461458d482a88d07b7955ddc1b2b4ff01ce0326660be30fa8bbaa1a339`  
		Last Modified: Thu, 18 Jun 2026 00:06:45 GMT  
		Size: 119.6 MB (119636266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa77a3ca10a502fb7b8748a1f9b29addf1ee1709c617702822b8ddc33366a234`  
		Last Modified: Thu, 18 Jun 2026 00:06:26 GMT  
		Size: 18.9 KB (18928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace78442516115eccbd3d3176b6dd887a0a0903b6e9128cf8837dd4f701fe812`  
		Last Modified: Thu, 18 Jun 2026 00:06:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ac22e63a5f7cf969858f2bcb545f99ec9d3886276a08e9f3c5ee8c17e92350`  
		Last Modified: Thu, 18 Jun 2026 00:06:26 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1427185813d21ca951af587c07e32bec2db6fb1a2df8917a7acd870004269c0`  
		Last Modified: Thu, 18 Jun 2026 00:06:27 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:54ca49c99b34078efb5fc70a7e2b81bac261803368ed2439a96a26e4f456e1a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.9 KB (655931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f89e430de8c136c807c0e3a6860d62bf51ae31f34dc948dd01f706f9daa92e`

```dockerfile
```

-	Layers:
	-	`sha256:423e2047dbd41133e0da32340322a622fd12a81f3f89f0bddf1b844195d2af4d`  
		Last Modified: Thu, 18 Jun 2026 00:06:26 GMT  
		Size: 615.8 KB (615755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee874d2f02f125c8f3fd7bfb99ba50695edc5d808789b1df6d2b6f61e7ace2f`  
		Last Modified: Thu, 18 Jun 2026 00:06:26 GMT  
		Size: 40.2 KB (40176 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.23` - linux; s390x

```console
$ docker pull postgres@sha256:dda37b024b64d1f063c01a37ecac6100c1c9a2ebe666944a00b7c19484e0b602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.1 MB (126066174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef58365d70858a132b1b99d8de9bb3cb9ab489c87e68689c40e1bbec6e35be67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:02:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 20:02:39 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 20:02:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 20:02:39 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 20:02:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 20:02:39 GMT
ENV PG_MAJOR=18
# Mon, 22 Jun 2026 20:02:39 GMT
ENV PG_VERSION=18.4
# Mon, 22 Jun 2026 20:02:39 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Mon, 22 Jun 2026 20:02:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 20:06:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 20:06:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 20:06:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 20:06:37 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 22 Jun 2026 20:06:37 GMT
VOLUME [/var/lib/postgresql]
# Mon, 22 Jun 2026 20:06:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:06:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 20:06:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:06:38 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 20:06:38 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 20:06:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f660c1c02d02731d9ba4ee7d28ce3f2c379403ab0ca5f5d653a92660f664d8be`  
		Last Modified: Mon, 22 Jun 2026 20:07:03 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369b7f3a61cb8d8356bbff1f10e34e0c4b369011a5ab8ac1cf5a637b5e5cf3ee`  
		Last Modified: Mon, 22 Jun 2026 20:07:03 GMT  
		Size: 874.5 KB (874489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2598b30e5055c8c3811a167ccb4c8ba20d680ff4b4f0d186472b4ad435ed53`  
		Last Modified: Mon, 22 Jun 2026 20:07:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a418577c65257f4f8c5780a822405cccd8aad2dbf26901bf036a1461136275ca`  
		Last Modified: Mon, 22 Jun 2026 20:07:05 GMT  
		Size: 121.5 MB (121458025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e61c83f397935bf28c69c4af4da96d4c18dd22455b6b0cd40868c552945bb97`  
		Last Modified: Mon, 22 Jun 2026 20:07:04 GMT  
		Size: 18.9 KB (18917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84189b84870d2ed9e765158cb2ebfcf78adb6687e2c73703ea1042ea19853ee9`  
		Last Modified: Mon, 22 Jun 2026 20:07:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc66ae8a97b3a174f63fff659dc4ac94cfc855b11cb890dc47dcc93afcd5274`  
		Last Modified: Mon, 22 Jun 2026 20:07:04 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0a8794ef426a4b644c0431a8edeb3eaa33ebba7bf0b170e3f317598f5b5ad3`  
		Last Modified: Mon, 22 Jun 2026 20:07:05 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:b913a0832b6d12b3d5fa4916759b13f7ef41f655125e4097565a35b612cb2709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.9 KB (655856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcddea973fd8c7a850d709d796814164b9863d8b878a59c6572390047a8f430`

```dockerfile
```

-	Layers:
	-	`sha256:03094e00ae7ac799b4957698f4bf31cdcac56d46c3b8d32bdbc6286aa73889e6`  
		Last Modified: Mon, 22 Jun 2026 20:07:03 GMT  
		Size: 615.7 KB (615731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0b5f8fdb81aa46b489181e15aa8503ca18e374b9d740753bcc7632e1266a29`  
		Last Modified: Mon, 22 Jun 2026 20:07:03 GMT  
		Size: 40.1 KB (40125 bytes)  
		MIME: application/vnd.in-toto+json
