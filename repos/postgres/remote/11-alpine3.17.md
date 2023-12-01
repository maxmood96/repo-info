## `postgres:11-alpine3.17`

```console
$ docker pull postgres@sha256:b038b2edf75e8cab030caba27cf619e1de9c60ff07b42b01c00b92bbe50600e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:11-alpine3.17` - linux; amd64

```console
$ docker pull postgres@sha256:2e6027efdaeab0ca1766b06934503337c5e726806bcda8bb6278b1bef95ce593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90282127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34e6a2aaf6089169de82aecd5ca022f1eedf94b59100e89ba1d7c000aa46b3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 19:02:26 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_MAJOR=11
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_VERSION=11.22
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_SHA256=2cb7c97d7a0d7278851bbc9c61f467b69c094c72b81740b751108e7892ebe1f0
# Thu, 09 Nov 2023 19:02:26 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"11.22","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@11.22?os_name=alpine&os_version=3.17"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:02:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:02:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e4aeb2a016082eacb6522c534481466559a3acdd0acd8c6478360b9bfdc52d`  
		Last Modified: Fri, 01 Dec 2023 00:14:24 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bc2932e1a20107166df762e50125a9f1274a3d41595ec66d0dd3c0e610229e`  
		Last Modified: Fri, 01 Dec 2023 00:14:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0625ef4d68a89b4d0045ec7dbd4a19d31de566eec86d480cd234dbb40e363f5`  
		Last Modified: Fri, 01 Dec 2023 00:14:25 GMT  
		Size: 86.9 MB (86888368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de067b64ac3d90d8ba8a46edbcd365239511e99f042cabe476314bae9ff582e3`  
		Last Modified: Fri, 01 Dec 2023 00:14:24 GMT  
		Size: 8.0 KB (7983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4646039ac063a39832deb309c31bf7c6e00aef2cd3e70dbb5643f9903cab2df8`  
		Last Modified: Fri, 01 Dec 2023 00:14:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2f7ab1d4613ebbae99c62bcae6c3089dab82c2ccdec88ec99677db1b79e01c`  
		Last Modified: Fri, 01 Dec 2023 00:14:25 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4e7ab01d38a95e30acb0b95c836959ccda6fe9716dad3b7ed2524f5cfefcba`  
		Last Modified: Fri, 01 Dec 2023 00:14:25 GMT  
		Size: 4.8 KB (4783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:041fc6fde3e4e55bb3d29558b75f369ad6bb4c191fc91755094dfd9280569585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.3 KB (841272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718acc6d9a3f9f627c41e7431461f2527668c33e8b39d9ae71736ff7734927f2`

```dockerfile
```

-	Layers:
	-	`sha256:0a97d9f00a8859889441c118a2f6185ea751e11087ebf2f3b23e7fee429332a7`  
		Last Modified: Fri, 01 Dec 2023 00:14:24 GMT  
		Size: 806.2 KB (806177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d96f6e765242771884ebf5cfe6f2afe8aba0f5d72323ccbcaa66a6734598e4`  
		Last Modified: Fri, 01 Dec 2023 00:14:24 GMT  
		Size: 35.1 KB (35095 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-alpine3.17` - linux; arm variant v6

```console
$ docker pull postgres@sha256:425d026545ffcc7556ce2c36513761024258c3ec77e7432e57e0d2e31afc6074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88137712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374b213976dc505c9dff128c5c51629ccdd0cd414610a43d99ab54e4e6960745`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 19:02:26 GMT
ADD file:90d3bdc6a557ead63796de0110e2fda87e65aa091070cbae612dfb2126568253 in / 
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_MAJOR=11
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_VERSION=11.22
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_SHA256=2cb7c97d7a0d7278851bbc9c61f467b69c094c72b81740b751108e7892ebe1f0
# Thu, 09 Nov 2023 19:02:26 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"11.22","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@11.22?os_name=alpine&os_version=3.17"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:02:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:02:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f0440ff44d712e5fc701b84856116589b428157893ac461b633b1ab30b627eed`  
		Last Modified: Thu, 30 Nov 2023 22:49:52 GMT  
		Size: 3.1 MB (3113003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6cf4f8e676ee69efccd3326170b642d4821da96caa3d84ab15fed2d10e82d03`  
		Last Modified: Fri, 01 Dec 2023 12:38:43 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206833baca681b868d0cc0287361c32c09607f21a4c46269b488cac9ad8077b5`  
		Last Modified: Fri, 01 Dec 2023 12:38:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409c9b2e2782f32a38a3dd51a9b16bf87d81711fe54605b80ba71d101c39838c`  
		Last Modified: Fri, 01 Dec 2023 13:09:46 GMT  
		Size: 85.0 MB (85010276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ec019bcd0e2ced1960dd3e4e90a82e9c121312f3a7b0b0a49a1353ff5aa5bb`  
		Last Modified: Fri, 01 Dec 2023 13:09:34 GMT  
		Size: 8.0 KB (7981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcab90e097bf695a92d6018e17015fbefd5534fc9ad1e4f5b10ea69c93bafb06`  
		Last Modified: Fri, 01 Dec 2023 13:09:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f8a59bc871e7145d52b3d8b02a39e6aa981d5871bda813f3095b80d55d0b68`  
		Last Modified: Fri, 01 Dec 2023 13:09:34 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275bf0f4c3941b49522029a6195dba0ca4d36c79b2d9c6d9f432ee72bd3b3249`  
		Last Modified: Fri, 01 Dec 2023 13:09:34 GMT  
		Size: 4.8 KB (4783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine3.17` - linux; arm variant v7

```console
$ docker pull postgres@sha256:3090982604567f14666f760aa987eef5c2e9bf91d219dee3c454e570602c0da4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82938766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c78e54ead7c1f3f04935ddb90951706c09b2e66dd770ed61c61fcc2a7cd73a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 19:02:26 GMT
ADD file:02a6ccbee2a71a547141a8480f3a3912c7bb0934df31124f4a4720204d326698 in / 
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_MAJOR=11
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_VERSION=11.22
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_SHA256=2cb7c97d7a0d7278851bbc9c61f467b69c094c72b81740b751108e7892ebe1f0
# Thu, 09 Nov 2023 19:02:26 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"11.22","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@11.22?os_name=alpine&os_version=3.17"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:02:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:02:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d4ee79c42f17f258e1c67dc32e0776c934799d208cd0a9b6264f65d60f1a26fc`  
		Last Modified: Thu, 30 Nov 2023 22:50:08 GMT  
		Size: 2.9 MB (2869713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daac7579ae28a407bb0d0a9db156253f5a411f5a6247ae429a4016d6c83c8b7b`  
		Last Modified: Fri, 01 Dec 2023 11:06:26 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da7d87480054885d297e6e92334e8ce5ae4651ef7205b73ec344642632e87cd`  
		Last Modified: Fri, 01 Dec 2023 11:06:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741dd4c0b90780824d403176e42cd9e9653e4d0ac855a4aee36c9838032cdd5b`  
		Last Modified: Fri, 01 Dec 2023 11:42:08 GMT  
		Size: 80.1 MB (80054619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d251d1f033109b3aa101cc164325e8e955a0d5da8427607738f6757174ea41d`  
		Last Modified: Fri, 01 Dec 2023 11:42:05 GMT  
		Size: 8.0 KB (7981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97d0670c5113381088c73297eb7eef5622128f9ae000a12b79750cc810473d0`  
		Last Modified: Fri, 01 Dec 2023 11:42:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be76c1d2f4f54bcfeff161aebaf39eaf3b072177b4c017216edcd6a60468b41a`  
		Last Modified: Fri, 01 Dec 2023 11:42:05 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b7fe858063b51d1a22306da9d7be68318fa573cedc90585baa8d29c3b64220`  
		Last Modified: Fri, 01 Dec 2023 11:42:06 GMT  
		Size: 4.8 KB (4784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:53df286feee244d449db4ca138fc7727684a077fbadef9f31c779432a9798816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.2 KB (841245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254bf9e31e22c37776b05ecdecd2c8d9fa141123101f1e0d39cf7d237c4267a8`

```dockerfile
```

-	Layers:
	-	`sha256:b1c7862a3e63c12469f998fc71e77cfd5e15085e0fc643797453c999220ea7e6`  
		Last Modified: Fri, 01 Dec 2023 11:42:06 GMT  
		Size: 806.2 KB (806197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10702ac17530453b3db1d7d1476a664e24c31b1ca7abcac4db77062b9751df18`  
		Last Modified: Fri, 01 Dec 2023 11:42:05 GMT  
		Size: 35.0 KB (35048 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:dcb7ac2f0014690dd48bdf41b770a12986b77bc0fed46198ec99461d55bc32ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88097482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b0ec45b32018508e667f953f3502be75b586194517da16b7b543959b2d30ea5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 19:02:26 GMT
ADD file:e5c66967d6570e36da50c9d42dd8f8f55e6c6a65b92c79601ea9e750c076fa2a in / 
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_MAJOR=11
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_VERSION=11.22
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_SHA256=2cb7c97d7a0d7278851bbc9c61f467b69c094c72b81740b751108e7892ebe1f0
# Thu, 09 Nov 2023 19:02:26 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"11.22","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@11.22?os_name=alpine&os_version=3.17"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:02:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:02:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b8180c93b172865af87a7c0e7e3c8bcb139e0d0c92e19c96467ff2cd4c8919ad`  
		Last Modified: Thu, 30 Nov 2023 23:11:45 GMT  
		Size: 3.3 MB (3258348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892bc68cc76cc391a887c761eb4892aef44e4199974b3cccf658f41ad2c41d74`  
		Last Modified: Fri, 01 Dec 2023 13:29:38 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b809b35e3ecb592d0cef272df76134a11a4eed8dbde6629cd97bf414099e77`  
		Last Modified: Fri, 01 Dec 2023 13:29:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe17d40c2f5262aa782a378d7de4af904e64de13f1c5c56e86d082827774985`  
		Last Modified: Fri, 01 Dec 2023 14:08:33 GMT  
		Size: 84.8 MB (84824699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4ecd957a53da416a1ca642299ba12f4175869a701432f429078adb51a2d161`  
		Last Modified: Fri, 01 Dec 2023 14:08:30 GMT  
		Size: 8.0 KB (7983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed39367226dfdbfada858227b424c86c310c8470e9ef5369f40824ca70b799c`  
		Last Modified: Fri, 01 Dec 2023 14:08:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8e546305ac81397927dafbeae03c4239e9e0b8b2da9a430c13f14b475a0808`  
		Last Modified: Fri, 01 Dec 2023 14:08:30 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ec1e36b70cb3ee8a7831b7af8e3544cef7eb9740be19fad3c21ee99739c076`  
		Last Modified: Fri, 01 Dec 2023 14:08:32 GMT  
		Size: 4.8 KB (4785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:eecaca54af4597bee1a5c1585916d39537810bf6893e658791c4638ad4171589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.1 KB (841119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e65e8484287afb2cbd17560fa6f51daba6d55aa0e01232f17fe0842327f594fd`

```dockerfile
```

-	Layers:
	-	`sha256:276c108748f9f523788ad33b91ccfb31b44f03829bf5b856619d620377f4b821`  
		Last Modified: Fri, 01 Dec 2023 14:08:31 GMT  
		Size: 806.2 KB (806184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e41dd9de3c56e3c655f3a84eabcef842775c401452c96475b99d71e8c78bfa03`  
		Last Modified: Fri, 01 Dec 2023 14:08:30 GMT  
		Size: 34.9 KB (34935 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-alpine3.17` - linux; 386

```console
$ docker pull postgres@sha256:f4d886f7db2b5828a3359a401d5a10ed6f3ef1aaec67536960d60c97e35f02ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96965087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc863cad29e406194b3827cd411a312c00e28ebe3de52a93145ccb321e754a3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:30 GMT
ADD file:437e2411fa3e4795a759f54507f41caa000169f0c32600ec49b4397313cd0884 in / 
# Mon, 07 Aug 2023 19:38:30 GMT
CMD ["/bin/sh"]
# Wed, 04 Oct 2023 14:54:45 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
ENV LANG=en_US.utf8
# Wed, 04 Oct 2023 14:54:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_MAJOR=11
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_VERSION=11.21
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_SHA256=07b0837471d5dd77b25166b34718f3ba10816b6ad61e691e6fc547cf3fcff850
# Wed, 04 Oct 2023 14:54:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 04 Oct 2023 14:54:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"11.21","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@11.21?os_name=alpine&os_version=3.17"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 04 Oct 2023 14:54:45 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 04 Oct 2023 14:54:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Oct 2023 14:54:45 GMT
STOPSIGNAL SIGINT
# Wed, 04 Oct 2023 14:54:45 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 04 Oct 2023 14:54:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ddc7d64c528fabaad61cc880e91abba829973f743d753415145211971f9ee10d`  
		Last Modified: Mon, 07 Aug 2023 19:39:10 GMT  
		Size: 3.4 MB (3413779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6192212658b761b7aca241a17fcb826fb268ccf46c8cf6ae152f1f5613e6ecbd`  
		Last Modified: Tue, 17 Oct 2023 19:07:51 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ed44aa59686a2bd4d65cf0023ad54a5f191f0688b19043b1682cebbfb64e5e`  
		Last Modified: Tue, 17 Oct 2023 19:07:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50f9ab35945a88ad76fc20d88edb1b6a4ccd23c336f33e3d6625646206e68d3`  
		Last Modified: Tue, 17 Oct 2023 19:07:59 GMT  
		Size: 93.5 MB (93536874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a7178a79ae461fefc0525b328266e9dcdff425ecf27f157669d20df3a334f6`  
		Last Modified: Tue, 17 Oct 2023 19:07:51 GMT  
		Size: 8.0 KB (7980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c9b26e6c7b5605ae135b9a5674f1cda2f610d1c53edd1a5e9f75fb9a9d039c`  
		Last Modified: Tue, 17 Oct 2023 19:07:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fccaf5e1ea6e70928d3e77612cde29b4a3ba800ff08c9aa56a8988c9059b44`  
		Last Modified: Tue, 17 Oct 2023 19:07:52 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f09d739db4848d1419567e5352c57328e1d7dd1548bc926625109a336ee8392`  
		Last Modified: Tue, 17 Oct 2023 19:07:52 GMT  
		Size: 4.8 KB (4784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:0ecea95ae9ea47c8a38940f84b39e0a0a6dc7119e60f81e3e3a387f9e3ddf146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.9 KB (34851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b82def37eb1bd9bdf38f073c9fe6b9b46b0fb9852cd153eada64e4d267f8ca`

```dockerfile
```

-	Layers:
	-	`sha256:55b0ea17d4c10929992b918ea0d0888351299b0ff97ca68437674cfea1fc006a`  
		Last Modified: Tue, 17 Oct 2023 19:07:51 GMT  
		Size: 34.9 KB (34851 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-alpine3.17` - linux; ppc64le

```console
$ docker pull postgres@sha256:c2fe2d69f4993c1fe15833b585236d62cb917d99389a32321ab353220d34454f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95898101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a045809c5527831bc1188a275bb18040d02de439b73653ba49fd5f731d5430`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 19:02:26 GMT
ADD file:e3eb0ea4f652282ad08228d0d146f33998b9e93641756d780ac0205aa828c070 in / 
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_MAJOR=11
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_VERSION=11.22
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_SHA256=2cb7c97d7a0d7278851bbc9c61f467b69c094c72b81740b751108e7892ebe1f0
# Thu, 09 Nov 2023 19:02:26 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"11.22","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@11.22?os_name=alpine&os_version=3.17"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:02:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:02:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c7d387f1f267ea360529df8d70b246f949e1afdb2317cdf84b028cda80a093d1`  
		Last Modified: Thu, 30 Nov 2023 23:20:17 GMT  
		Size: 3.4 MB (3391875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eefd687ec695dbf5ad2ea3426f89c171644eeb6b8a2f5ca1f82d86789dd7e67`  
		Last Modified: Fri, 01 Dec 2023 12:12:39 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310619b08e66325eab5686b9b75b3fa3bbfbf31403f2be9f5b491fb5189cc7ef`  
		Last Modified: Fri, 01 Dec 2023 12:12:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260bc043700f6838baf6ea53b195bcf04f58ff8d020a8673ce44ac1ce2818ca6`  
		Last Modified: Fri, 01 Dec 2023 12:49:22 GMT  
		Size: 92.5 MB (92491781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f45998c4f0bd91b4f70aa4a8159e96bc27d62d7eaa4fb1072ce9d29dccb8a1`  
		Last Modified: Fri, 01 Dec 2023 12:49:18 GMT  
		Size: 8.0 KB (7989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2388537b4e8fd0ebe0322dc8b4425e1711d0c8c5d415bcd0c8e2bc881fe3b42`  
		Last Modified: Fri, 01 Dec 2023 12:49:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4df0a888fa72d6343c4498c86249fcd87ae78f5c7e96e7be707593715c3ca18`  
		Last Modified: Fri, 01 Dec 2023 12:49:18 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8486ddbe7a71bcc7a8dff067746d28517cda7eb329eaa7efbb71ba137c095b`  
		Last Modified: Fri, 01 Dec 2023 12:49:19 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:ec1977e1333ce6d0813ebe6a761f9468a9ac5dfc44f4ee3d36d0697e4bed5e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.1 KB (838113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2930b86d8af2a5dd95552eeec8da148133c39643e6d3a9b5023e4273c768ef02`

```dockerfile
```

-	Layers:
	-	`sha256:ea61bbc9e067146647c4f8fe9fe78c082820756743cfc23972a88f7b25b4ba35`  
		Last Modified: Fri, 01 Dec 2023 12:49:19 GMT  
		Size: 803.1 KB (803148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:032cf1632b93e004e52141fff268c4b56ed49a96da9d1418f04816be0cc8f336`  
		Last Modified: Fri, 01 Dec 2023 12:49:18 GMT  
		Size: 35.0 KB (34965 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-alpine3.17` - linux; s390x

```console
$ docker pull postgres@sha256:fc6c9458bbc985fcb207521aea00889d4095a3bf4c3da4834d34b623f9ac315d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90722644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691257a90e3f05868adf9848f92b410fa211ca2aa172cb43bea951fb601b2769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 19:02:26 GMT
ADD file:bf416048d22b9a0deecb508385355d79b8d5d12b655c600dbdc0948f7dcbb2c2 in / 
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["/bin/sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_MAJOR=11
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_VERSION=11.22
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_SHA256=2cb7c97d7a0d7278851bbc9c61f467b69c094c72b81740b751108e7892ebe1f0
# Thu, 09 Nov 2023 19:02:26 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"11.22","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@11.22?os_name=alpine&os_version=3.17"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:02:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:02:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7e9e7e53b618240d2e82e8cab6b677eab6786c4210dcc2b1a35bfd4cb492757e`  
		Last Modified: Thu, 30 Nov 2023 22:43:01 GMT  
		Size: 3.2 MB (3176332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3104d6f3f1d533a0d4fb71b4dc15da4cf1ef964a88da6bd5ad2d31b5e916d67`  
		Last Modified: Fri, 01 Dec 2023 11:20:51 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492a581271ed07263f2c3709798fdf8d8a07f0e2354d9388a2a9bed66520b756`  
		Last Modified: Fri, 01 Dec 2023 11:20:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7c291ea85de93834cc82f79aaae422bab6193d9ba224969fc0076d227d6a0f`  
		Last Modified: Fri, 01 Dec 2023 12:07:26 GMT  
		Size: 87.5 MB (87531866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ecb97448e7f5d61f95b35dcac97c398d5835ba56087044be3024fb992e0627`  
		Last Modified: Fri, 01 Dec 2023 12:07:24 GMT  
		Size: 8.0 KB (7988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff41eb6c1b6036def1f2ff5edb35163fe67d9bca6b64f4168b8db3c4f9abf3b`  
		Last Modified: Fri, 01 Dec 2023 12:07:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60214cd8d253a945a02259bddea5b362f19e81909085b739947dfcdaaf276624`  
		Last Modified: Fri, 01 Dec 2023 12:07:25 GMT  
		Size: 164.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf516b3b9d55b76119f9860b6170d8e174586c08102c6a65f500b88a1709745`  
		Last Modified: Fri, 01 Dec 2023 12:07:25 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-alpine3.17` - unknown; unknown

```console
$ docker pull postgres@sha256:fbf315bb6f9491405501cde0eebf4a3cb82c67683f8fbc91e3b4b95b0eff0665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **839.5 KB (839470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfef782f72bf627a7c3659b5a628c306ebdd57b3f8b98ca4c02c455afd89f97`

```dockerfile
```

-	Layers:
	-	`sha256:ad8fd607433769f36a7ef327962995ea3c33b0783adcd80e8fd6109c4b8f28d9`  
		Last Modified: Fri, 01 Dec 2023 12:07:24 GMT  
		Size: 804.5 KB (804541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de992661315025de80ea1ed14afea4f92d690fd3693af90c82180c933521898e`  
		Last Modified: Fri, 01 Dec 2023 12:07:24 GMT  
		Size: 34.9 KB (34929 bytes)  
		MIME: application/vnd.in-toto+json
