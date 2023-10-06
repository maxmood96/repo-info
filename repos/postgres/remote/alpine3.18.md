## `postgres:alpine3.18`

```console
$ docker pull postgres@sha256:457c6deb88f9030fcf106a954ee548ca5bf801d6cbdf48b3ea538202d2a9693b
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

### `postgres:alpine3.18` - linux; amd64

```console
$ docker pull postgres@sha256:5deffe73283baaee8571c78c4cbc677db01bfc5a0de6cd70800c61d812c71810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94243334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d837b93a1c9b6a19da1b31e246e9a7cb9a09f20857c8b7429e029f7d4c5a40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Wed, 04 Oct 2023 14:54:45 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
ENV LANG=en_US.utf8
# Wed, 04 Oct 2023 14:54:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_MAJOR=16
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_VERSION=16.0
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_SHA256=df9e823eb22330444e1d48e52cc65135a652a6fdb3ce325e3f08549339f51b99
# Wed, 04 Oct 2023 14:54:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 04 Oct 2023 14:54:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"16.0","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@16.0?os_name=alpine&os_version=3.18"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
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
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7e9d0e60f3df67a659b0743ab2dcbaa55c722fba908ad77072b9d436726779`  
		Last Modified: Fri, 06 Oct 2023 01:04:33 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9538d5302eee66c89f985c5558395a53a65381428baf65fa30790409b0434abd`  
		Last Modified: Fri, 06 Oct 2023 01:04:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddefdf18815a6fd65c6c1f4d6896146d2d80ab0d9c421299f110d3966970d22e`  
		Last Modified: Fri, 06 Oct 2023 01:04:37 GMT  
		Size: 90.8 MB (90825348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483d47e7b8465251ba9734114670127198521ce460ed833137ec8df2c6486d11`  
		Last Modified: Fri, 06 Oct 2023 01:04:33 GMT  
		Size: 9.6 KB (9558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f69e6f6f92ec3623270a6c11dbf7e6fecdcd94b7b884562167d43b0483d3810`  
		Last Modified: Fri, 06 Oct 2023 01:04:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad5f543b2cbea94dfa33bf07e1b3738abe7817ea81c148092e471e1141183f3`  
		Last Modified: Fri, 06 Oct 2023 01:04:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f41102d57346a5b127164c6a54850ba8823b329f907918b9e7566a0ffca1059`  
		Last Modified: Fri, 06 Oct 2023 01:04:34 GMT  
		Size: 4.8 KB (4784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:734f02d586f6fb83f91f964a6df9ecc50fce1c62871d5988d780c1c798609332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.4 KB (873385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9803fdea719fb08b3cf6c9ae7b00f1e6720cad27e8a7481e0aa79ab1e7093cbc`

```dockerfile
```

-	Layers:
	-	`sha256:18fb0f012bff55efbc1f2fcdb6957ba7f496a0ae1376980c3823aa74bb6daa5c`  
		Last Modified: Fri, 06 Oct 2023 01:04:33 GMT  
		Size: 836.6 KB (836551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d69d765f75abefb1f02f44fa6f52eb5d5bfe61b381351d33030067c8328d930`  
		Last Modified: Fri, 06 Oct 2023 01:04:33 GMT  
		Size: 36.8 KB (36834 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.18` - linux; arm variant v6

```console
$ docker pull postgres@sha256:bad2f13419ae13efb1efa1626fb7f19d3c54d22c4b9f5b3314c3bb53f3e74dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92873351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cfc6254f20df0ed78296b33c1d6db7688924067c8c641e60484f7a256f7191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Wed, 04 Oct 2023 14:54:45 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
ENV LANG=en_US.utf8
# Wed, 04 Oct 2023 14:54:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_MAJOR=16
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_VERSION=16.0
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_SHA256=df9e823eb22330444e1d48e52cc65135a652a6fdb3ce325e3f08549339f51b99
# Wed, 04 Oct 2023 14:54:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 04 Oct 2023 14:54:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"16.0","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@16.0?os_name=alpine&os_version=3.18"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
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
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f9677461cc1446c142c4f11c5e5ba7ae5eb0160b5884c6c4703d8bbc271706`  
		Last Modified: Fri, 29 Sep 2023 17:11:50 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da301824fff35c4518ffe54b8851eeba7f52fe7519c55c3daee52a26301b52c`  
		Last Modified: Fri, 29 Sep 2023 17:11:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788f20ee7cddd452fd415482d364e8f1132f071bc09f84b940dba31a945adf52`  
		Last Modified: Fri, 06 Oct 2023 01:06:08 GMT  
		Size: 89.7 MB (89712044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0a79757dff81e0f626036be6ef9786c30518222730db3034d524790f4a123b`  
		Last Modified: Fri, 06 Oct 2023 01:05:52 GMT  
		Size: 9.6 KB (9558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7fb9f7703a05bed5ee47fd0e6e16f2cc024e841d994a684b8ef137aa56d7536`  
		Last Modified: Fri, 06 Oct 2023 01:05:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2d44ae2c34dbeb2d522dc848324d40c2bae94e07000bd463299e7bebaa0906`  
		Last Modified: Fri, 06 Oct 2023 01:05:52 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152f9724d9804a2d32d9a4a2ab3ccbb397e1b9ea8d816d752a3bfa034d39c50f`  
		Last Modified: Fri, 06 Oct 2023 01:05:52 GMT  
		Size: 4.8 KB (4782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine3.18` - linux; arm variant v7

```console
$ docker pull postgres@sha256:599c2100b845f12fd99d81550fba5efee2fa1235cfcb7d50def23ff30e78fc56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87531525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20217d59d2e1b4b521f49df2bb0c24ba7177a3b2997eddf0590dd14097ca9f42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 14 Sep 2023 18:21:14 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 14 Sep 2023 18:21:14 GMT
CMD ["/bin/sh"]
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV LANG=en_US.utf8
# Thu, 14 Sep 2023 18:21:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PG_MAJOR=16
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PG_VERSION=16.0
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PG_SHA256=df9e823eb22330444e1d48e52cc65135a652a6fdb3ce325e3f08549339f51b99
# Thu, 14 Sep 2023 18:21:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Sep 2023 18:21:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Sep 2023 18:21:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Sep 2023 18:21:14 GMT
STOPSIGNAL SIGINT
# Thu, 14 Sep 2023 18:21:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Sep 2023 18:21:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de34561774cc0a52beeb06fef6a1f6af2bd2a08d4ea304d8d6da8fca56b666f`  
		Last Modified: Fri, 29 Sep 2023 17:52:13 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f40d1b3c22c63e3341b41845b4002cf47594b6e022558becb3c12725dbea465`  
		Last Modified: Fri, 29 Sep 2023 17:52:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1593a9a6ee8dde9fc31f8e6ddf305285eb2a75616ff76bde20f2e031b41d77`  
		Last Modified: Fri, 29 Sep 2023 17:52:16 GMT  
		Size: 84.6 MB (84615593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852ac5cb9f2c5ef3ee3ad63d1088f80a9064156b70c794d1e9a504d04c647f7c`  
		Last Modified: Fri, 29 Sep 2023 17:52:13 GMT  
		Size: 9.6 KB (9567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dddb8f7c5ca9b91506344516e7a080dfe3cbf680f1e734ce54aac3dfca95e21`  
		Last Modified: Fri, 29 Sep 2023 17:52:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c167e5573b29c9955943a56e23f4496b6e392984d4f9f0490c8542fdfc1dd9e9`  
		Last Modified: Fri, 29 Sep 2023 17:52:14 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd3b699a79e1e56043286a264228cac7643adcc02f7a206f0044a0bbdb44eb`  
		Last Modified: Fri, 29 Sep 2023 17:52:14 GMT  
		Size: 4.8 KB (4788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:9457bd18ec7a3cfa509befed4e953d93dd8cfa94681fbdaa697ee57ead487bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.3 KB (871322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c939261253e2c4e41dadeab815e3fc90d49a11f9062f8ea387701e3c2df93d45`

```dockerfile
```

-	Layers:
	-	`sha256:c09f4a787772c57e1a9249191e367432653153d7b6876cef5702b1216faeab03`  
		Last Modified: Fri, 29 Sep 2023 17:52:13 GMT  
		Size: 835.5 KB (835542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:091a810f6b3866a9379ba384037f107d05908d4b68dd47dd3035339797112644`  
		Last Modified: Fri, 29 Sep 2023 17:52:12 GMT  
		Size: 35.8 KB (35780 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:65b5b36a2efdec783140ab6921f58a3f303c7c531132d2b7cdd8c544ff1e8666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93179579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe33c956322ac05801374521b512e525a4046a9308d0d25946999b6ba0a8e7b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 14 Sep 2023 18:21:14 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 14 Sep 2023 18:21:14 GMT
CMD ["/bin/sh"]
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV LANG=en_US.utf8
# Thu, 14 Sep 2023 18:21:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PG_MAJOR=16
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PG_VERSION=16.0
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PG_SHA256=df9e823eb22330444e1d48e52cc65135a652a6fdb3ce325e3f08549339f51b99
# Thu, 14 Sep 2023 18:21:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Sep 2023 18:21:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Sep 2023 18:21:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Sep 2023 18:21:14 GMT
STOPSIGNAL SIGINT
# Thu, 14 Sep 2023 18:21:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Sep 2023 18:21:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57128d869f4112bd058a44bc2fd19d9b05ea0895b34ad51c07e45ddadd30d480`  
		Last Modified: Fri, 29 Sep 2023 17:14:32 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1755e5b66878a2e0b911de75610a642179f0862fd67d7ac96105919310c7ee6`  
		Last Modified: Fri, 29 Sep 2023 17:14:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601e91665cba1da62c9d83f36f555adb896a99a11877b3c145770b81acac19db`  
		Last Modified: Fri, 29 Sep 2023 17:14:35 GMT  
		Size: 89.8 MB (89831726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e568d75b43a7eed39d5621c9d4bf2936c347475d0c1289f7b01578ceebeccd65`  
		Last Modified: Fri, 29 Sep 2023 17:14:32 GMT  
		Size: 9.6 KB (9565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584a4487d7a902e3adb748850efcc8851c08b9aaa5fc0f08af3c8d18f43c7b0f`  
		Last Modified: Fri, 29 Sep 2023 17:14:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfeec5c3ddac4cd5dfc89bda670b11487c045884d57ab3efa6fa0e6ee89b2baa`  
		Last Modified: Fri, 29 Sep 2023 17:14:33 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296ea965c81a3ca81dab805cfdebd1d6e8c6340f3c30840eb55bf17826f4c9ec`  
		Last Modified: Fri, 29 Sep 2023 17:14:33 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:207896381d71059886fcdb1776d31336086aa025711f88af004e5dc9a2e6c0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.2 KB (871153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9764accba8a212844afadc07f38e534d8676bf20ef19ce1604c9a327b9965eb`

```dockerfile
```

-	Layers:
	-	`sha256:2ebf244b868b30cb4422f45d21b8b4dabbea75e05fb2ac6962b53bd57a74daf7`  
		Last Modified: Fri, 29 Sep 2023 17:14:32 GMT  
		Size: 835.5 KB (835509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6aa31f4ddac6031722f859918c57cf7582af70cb50af416a700d23f20bb5f57`  
		Last Modified: Fri, 29 Sep 2023 17:14:32 GMT  
		Size: 35.6 KB (35644 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.18` - linux; 386

```console
$ docker pull postgres@sha256:82dfb36e10635d69baa51dfbc4327c0431271eb0afd305c3233cf226ccfb47f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99208010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a678751bc3b051a8a31b9f34465ec7a0ab072045cf385c3efd70808a5177537`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 28 Sep 2023 20:38:19 GMT
ADD file:8402753f294e403e92353bd65c86a6428c960be5116c0a15484b663a84f66fcd in / 
# Thu, 28 Sep 2023 20:38:20 GMT
CMD ["/bin/sh"]
# Wed, 04 Oct 2023 14:54:45 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
ENV LANG=en_US.utf8
# Wed, 04 Oct 2023 14:54:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_MAJOR=16
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_VERSION=16.0
# Wed, 04 Oct 2023 14:54:45 GMT
ENV PG_SHA256=df9e823eb22330444e1d48e52cc65135a652a6fdb3ce325e3f08549339f51b99
# Wed, 04 Oct 2023 14:54:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 04 Oct 2023 14:54:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 	echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"postgres-sbom","packages":[{"name":"postgres","versionInfo":"16.0","SPDXID":"SPDXRef-Package--postgres","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/postgres@16.0?os_name=alpine&os_version=3.18"}],"licenseDeclared":"PostgreSQL"}]}' > /usr/local/postgres.spdx.json 	; 	postgres --version # buildkit
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
	-	`sha256:dc95107ad2a031a015320bb397f73ec151d738127175b31ad643120697dc7e90`  
		Last Modified: Thu, 28 Sep 2023 20:39:32 GMT  
		Size: 3.2 MB (3235757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1880227f90c4d2f833c91b12e6785637aae98a1c15694fd7125cb3da2657a6ef`  
		Last Modified: Fri, 06 Oct 2023 01:07:53 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fc5619727425bc9d13e9e2c4200de273dd38cec4956d2f7d4a10e4fa3d90dd`  
		Last Modified: Fri, 06 Oct 2023 01:07:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930553606c72d4c611ab89ec12b9131ea251b4a2e854b8ce18bf96efc9c93b1c`  
		Last Modified: Fri, 06 Oct 2023 01:07:57 GMT  
		Size: 96.0 MB (95956236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ec7616fee7b908e3c4676a5c50523be68f0af4e76cff3df3f15940c96f3f85`  
		Last Modified: Fri, 06 Oct 2023 01:07:53 GMT  
		Size: 9.6 KB (9558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c353505ed7ab01dd78b32e9fd489cd59d2667fde5022be489679e33654b6e9`  
		Last Modified: Fri, 06 Oct 2023 01:07:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4f6be0a9a8bf9524fc680dba6c4b8cbca7d0b9d40a29e5cf6d277cbc2db5f3`  
		Last Modified: Fri, 06 Oct 2023 01:07:54 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d1173f5c4215431551d04e4a352ed1c297814eca7c6f95c99d3a1436865bd0`  
		Last Modified: Fri, 06 Oct 2023 01:07:54 GMT  
		Size: 4.8 KB (4783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:7a0d10cbbe629b7f737be59c1af6766774e696fa2a7e043496b7056697b24d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4490c312e0060f8765a08083fe67a50cdf503d85b71e69387a67134b6af686c0`

```dockerfile
```

-	Layers:
	-	`sha256:119ec1f1a57ef3609ed680cbc9b2223f9d3657f5005efa45b0e03f2e85268a22`  
		Last Modified: Fri, 06 Oct 2023 01:07:53 GMT  
		Size: 36.6 KB (36571 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.18` - linux; ppc64le

```console
$ docker pull postgres@sha256:5f463f4890aecc313f28cf353659627689d3b41a9e2ff9d79bde0379c5967da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (99957234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e81c78455cfdc637c8d0518526f90b44f5e672e99e140787ee00ce8ab8346c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 14 Sep 2023 18:21:14 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 14 Sep 2023 18:21:14 GMT
CMD ["/bin/sh"]
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV LANG=en_US.utf8
# Thu, 14 Sep 2023 18:21:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PG_MAJOR=16
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PG_VERSION=16.0
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PG_SHA256=df9e823eb22330444e1d48e52cc65135a652a6fdb3ce325e3f08549339f51b99
# Thu, 14 Sep 2023 18:21:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Sep 2023 18:21:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Sep 2023 18:21:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Sep 2023 18:21:14 GMT
STOPSIGNAL SIGINT
# Thu, 14 Sep 2023 18:21:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Sep 2023 18:21:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0eda61a2703e25325ea1e358d3a74fe87529df79e6beb419567f1bdbbb63df`  
		Last Modified: Fri, 29 Sep 2023 17:20:30 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b29b4ecd4028475762890da3e105d2ad2bb7690a0bff52c89c3d7180aca779`  
		Last Modified: Fri, 29 Sep 2023 17:20:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72da0ebbc2f8105c34b4268f7c0c16d30c9914b2db243c165b984c05b10af610`  
		Last Modified: Fri, 29 Sep 2023 17:20:34 GMT  
		Size: 96.6 MB (96594699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335d575912a52f68c8251cc791230fa4057b8e7128737beace61ccb05c450d06`  
		Last Modified: Fri, 29 Sep 2023 17:20:30 GMT  
		Size: 9.6 KB (9569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae324d8420d80bf3aeb586596216c225d89b1fadeb83456d30ab907d7fdf2e1d`  
		Last Modified: Fri, 29 Sep 2023 17:20:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1e56bb94b0a6b13809e1b7b1cadeef342d509b8767803ac92df098e6809276`  
		Last Modified: Fri, 29 Sep 2023 17:20:31 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f72f9d38a4e0bdab010976c2a7c940c3764730691b9e159f044c1283c73b78`  
		Last Modified: Fri, 29 Sep 2023 17:20:31 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:4e311184cb24d0349ba2a729759ad98657c85885c6367b8b9276a4af43880b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.8 KB (867799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617e0c76b305bd411af7ccb13f22268461da6436fa9fbf063068653ad2eff356`

```dockerfile
```

-	Layers:
	-	`sha256:d854ab6b1eb4717bbd24578511184b53d21fe192e0a30cc6640fa4bc05e29daa`  
		Last Modified: Fri, 29 Sep 2023 17:20:30 GMT  
		Size: 832.1 KB (832109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa766b3575661a044d413930e27f58872f1decb437dc3b8aa0a7dd4011dac29f`  
		Last Modified: Fri, 29 Sep 2023 17:20:30 GMT  
		Size: 35.7 KB (35690 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.18` - linux; s390x

```console
$ docker pull postgres@sha256:9183a04f15b910edf4b3dda07f62ab332fd107d62c994efc51a5e0893573a9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95910829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef64d4ba34e4f4cc9bffacdcab9546fba42d21e21220c192b96f3c870b6d7c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 14 Sep 2023 18:21:14 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 14 Sep 2023 18:21:14 GMT
CMD ["/bin/sh"]
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV LANG=en_US.utf8
# Thu, 14 Sep 2023 18:21:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PG_MAJOR=16
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PG_VERSION=16.0
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PG_SHA256=df9e823eb22330444e1d48e52cc65135a652a6fdb3ce325e3f08549339f51b99
# Thu, 14 Sep 2023 18:21:14 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Sep 2023 18:21:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Sep 2023 18:21:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Sep 2023 18:21:14 GMT
STOPSIGNAL SIGINT
# Thu, 14 Sep 2023 18:21:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Sep 2023 18:21:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ae232bced3defb4eae7f5affb566ea50f50655d575488965e418a8da86b3ed`  
		Last Modified: Fri, 29 Sep 2023 18:03:31 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68a6f64e487e2750fccb626c86600fd10e0346eabb9bdb31da4b7824cac4a0b`  
		Last Modified: Fri, 29 Sep 2023 18:03:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0139a0b00eeca6b58c1d35b04e43e0bf759b96288a7c4dce26fc8756129fb28`  
		Last Modified: Fri, 29 Sep 2023 22:44:10 GMT  
		Size: 92.7 MB (92679699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5b20ffe1942c449162fffb045d081d766cb0526e9d44d80d37867e739a4ece`  
		Last Modified: Fri, 29 Sep 2023 22:44:05 GMT  
		Size: 9.6 KB (9565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36a69d699099cd9ad55f216d289b33ceeb24c69e73c5eb2f1b906490c0e2a9b`  
		Last Modified: Fri, 29 Sep 2023 22:44:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9676071d74f664b70b173c632b1f7bb42b76fd80dde50b5f65a49df111c4a8f`  
		Last Modified: Fri, 29 Sep 2023 22:44:05 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67d82951701fc0d2f7652913656545e7a2a155b9f33649afcc98fc9a7f2de23`  
		Last Modified: Fri, 29 Sep 2023 22:44:06 GMT  
		Size: 4.8 KB (4787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:fe187a7deb5b184c9d56080f124d2ec7b168ed3c4316b4dd48a39900014c698a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **869.2 KB (869190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5dc3b01c13f07b881dbb0371079e5214255bc0c4aef3ea8b17ebf04010af4d`

```dockerfile
```

-	Layers:
	-	`sha256:758b0481c29c72aa718f376f3014e92751328656f45b13cb7f94e124a6a26ccc`  
		Last Modified: Fri, 29 Sep 2023 22:44:05 GMT  
		Size: 833.6 KB (833560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9786d3266a9dd92c645ce36ab20ef479b61f1b29412759a4cfe44fdaa1243238`  
		Last Modified: Fri, 29 Sep 2023 22:44:05 GMT  
		Size: 35.6 KB (35630 bytes)  
		MIME: application/vnd.in-toto+json
