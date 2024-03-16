## `postgres:15-alpine3.18`

```console
$ docker pull postgres@sha256:795beb6ad0a39051fdd2edc3da605c8086c3e985df31c61968e1438d5f8418ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `postgres:15-alpine3.18` - linux; amd64

```console
$ docker pull postgres@sha256:d0358fad402f8ae59be5ad43faca32b51d65ba62f606b141ae0bd92855ae4270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93413936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fd977b1281abac51a5e566fad125c8a11a06eaa608d30337ad5c344fd24698`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_MAJOR=15
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_VERSION=15.6
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_SHA256=8455146ed9c69c93a57de954aead0302cafad035c2b242175d6aa1e17ebcb2fb
# Thu, 08 Feb 2024 19:40:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:40:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:40:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:40:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5003835903eec9df626a69e4a4dfe125bd043ca7f06083a5ae97ca82ffb906`  
		Last Modified: Sat, 16 Mar 2024 00:00:24 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48367c8c74468b7f471455bd65ef939fe8e6430cab2a6d69222b6744b3693b1`  
		Last Modified: Sat, 16 Mar 2024 00:00:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33894e5a6f7913e1e56debc64f19c73a2a4aabfb31d2dec959fceb5e66f64f55`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 90.0 MB (89994666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af5dc51d9d9d7c911f5a64f12f4295b3a9bbf82a1ab284e7556c89a035e4884`  
		Last Modified: Sat, 16 Mar 2024 00:00:24 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6866d4a6f5d7755e7d448eb846421df0b84ead62ce4e4cda45034de5ec20b275`  
		Last Modified: Sat, 16 Mar 2024 00:00:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6245998adc17a39905c98514e826bede4f0caa697e9aae40b91ca75747e3528`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d36c09773b16fd4a168820b1df6e3c651c088a4505c6556c568ac1625763b8b`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb194737c34f68bd613887723246b57eb71a3475a5b650c00822c45fefb15dff`  
		Last Modified: Sat, 16 Mar 2024 00:00:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:7aa816830c1dcd81cbf85d65e9117452cc64ebe75849ef138377087dbab8ce58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.3 KB (993293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1840a1663ab3973b5ac6d6aa21a6f47bd9d6698b9afaa02a36b351d53362201`

```dockerfile
```

-	Layers:
	-	`sha256:16ac38aa42860107d1dca3f85e10776b0c19abc950087de5920406c6a21b22b7`  
		Last Modified: Sat, 16 Mar 2024 00:00:24 GMT  
		Size: 956.1 KB (956068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba19c9c10865c01048c4e48b2e2533671e111c9dc1e1b4d8c42edf896c18e81e`  
		Last Modified: Sat, 16 Mar 2024 00:00:24 GMT  
		Size: 37.2 KB (37225 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.18` - linux; arm variant v6

```console
$ docker pull postgres@sha256:4ff5e51e620e44f3554fc0104f497d8ab2751205888c34f2bd414c181bc3b1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92097895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54ab7954600a26d8af5e3d9fe70eb5cee0885fbc561efd637a4e30fa539246e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_MAJOR=15
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_VERSION=15.6
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_SHA256=8455146ed9c69c93a57de954aead0302cafad035c2b242175d6aa1e17ebcb2fb
# Thu, 08 Feb 2024 19:40:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:40:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:40:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:40:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f162067667165927cc6eaee841a2797acf104d72473c6b32e22693a0897a64c5`  
		Last Modified: Mon, 12 Feb 2024 22:20:54 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15988adb2b9009a62352560910de674e1e39283cda96101ccf0328d84c0d5855`  
		Last Modified: Mon, 12 Feb 2024 22:20:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce32dfeee6f8317a17677f7caf7cfa14de0a6a8d44004b3ab2972f8f92a38f8`  
		Last Modified: Mon, 12 Feb 2024 22:27:47 GMT  
		Size: 88.9 MB (88934107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b1da03f08282d7ecf64412afd5b6a74295e61d9f33cfc6bc99b657fa6289c6`  
		Last Modified: Mon, 12 Feb 2024 22:27:45 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a82f4c24a748f9e0c5410335cb04a0f9dcb9422665399b73751205060cd2ab4`  
		Last Modified: Mon, 12 Feb 2024 22:27:45 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0939997ba8595ae328a3056ae2cba7c52016a1804cf028aea7d47fb9bcfa2856`  
		Last Modified: Mon, 12 Feb 2024 22:27:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6418b53b189a19d65c430f6b34d0747f7562d54d6a24d6abe72cf1f84f264`  
		Last Modified: Mon, 12 Feb 2024 22:27:46 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd02a6252a1d40c2d0cfa9ee77677e86ce5c0236a02c81bebb62933750bd76`  
		Last Modified: Mon, 12 Feb 2024 22:27:46 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:1d7f8a003295bb106f77f2591e8c88a72bc06e9b00170e689e87a783fc4d5157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 KB (36976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150d75f532cc6512eb5b3e4c74f9da3d8821bb2c31754772432de3447af04a07`

```dockerfile
```

-	Layers:
	-	`sha256:137bde391c7f40f115d1e11fa116444e8b45241fda688bef55c1b6193cb24b34`  
		Last Modified: Mon, 12 Feb 2024 22:27:45 GMT  
		Size: 37.0 KB (36976 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.18` - linux; arm variant v7

```console
$ docker pull postgres@sha256:e2d37a7071e4d5c80c8edd23cd5efc90183f0280421cae64de8b7de082c452b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86753436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462f960ab5e0827b94d21c72b19bad86a68da2d70b83be6b8fec5fd9b1142f2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_MAJOR=15
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_VERSION=15.6
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_SHA256=8455146ed9c69c93a57de954aead0302cafad035c2b242175d6aa1e17ebcb2fb
# Thu, 08 Feb 2024 19:40:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:40:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:40:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:40:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd3b6f1b54990dd494ffb1b65bf336b05d6f789f5529ff89482a0472262b2c3`  
		Last Modified: Tue, 13 Feb 2024 00:17:11 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd7cd37e35818f6d35c46b5ef95dd9a351c4be78e3edaac0624e39f0c4eb42d`  
		Last Modified: Tue, 13 Feb 2024 00:17:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e95a7c21ecf43c3b18a2dd7906571ff8d431900e1f92080693e8c51f8e04ac6`  
		Last Modified: Tue, 13 Feb 2024 01:19:07 GMT  
		Size: 83.8 MB (83835323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2217f10d2a29b7be6c27e37d8d308952f19ea0fac1483bb617f483b2071076`  
		Last Modified: Tue, 13 Feb 2024 01:19:04 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af6dbab427d7cff5d1f1edd4d5e06674f273e9a12d450d9cffa0c039717dc12`  
		Last Modified: Tue, 13 Feb 2024 01:19:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3923b0618ddcfdb6d2dc178226da7deda002dd83d9b167ac07108c4c0b26e930`  
		Last Modified: Tue, 13 Feb 2024 01:19:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbff73b9b90bbd20fd6b2ec0afb8788e5f846879ab03026c427a83c08760baa1`  
		Last Modified: Tue, 13 Feb 2024 01:19:06 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4145b936ea0889f2512eb0551658f83b28970bb179ed39bd1578ea975fd94f83`  
		Last Modified: Tue, 13 Feb 2024 01:19:06 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:e282627192bc02af15c30e637ce3f70b27e4899e5b0c2e9bdfd431c4a31838da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.4 KB (843395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe45bbce6fd9417ac884d7517e28b9800278257d0f6abfb601e6e66c1739d56c`

```dockerfile
```

-	Layers:
	-	`sha256:f80016f6e6a884174938d50490c1110b973f3a7f1f2bdeaacfbc9f81c1689ddf`  
		Last Modified: Tue, 13 Feb 2024 01:19:04 GMT  
		Size: 806.2 KB (806204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d2664438ffc5db0588e30926f20f7e55b9f3fddee34d03ccc7c7ec1cc687e8`  
		Last Modified: Tue, 13 Feb 2024 01:19:04 GMT  
		Size: 37.2 KB (37191 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:5aae041b97d6408baa0102a92da1df258ce1de2c886f77179d201fb0d8cd6423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92348404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785de63b4dcf8de4cfbf98c7f38f53ba90300b9dfea57f44ddad2a7c10fcb3ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_MAJOR=15
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_VERSION=15.6
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_SHA256=8455146ed9c69c93a57de954aead0302cafad035c2b242175d6aa1e17ebcb2fb
# Thu, 08 Feb 2024 19:40:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:40:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:40:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:40:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdffa6c2002e0e6756cd4a14b91c587ee3fa930e296bc42ec44324776923cdd2`  
		Last Modified: Tue, 13 Feb 2024 01:04:09 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fc7af1eb2e43aacadbb162cf37a3e4dba1f130de9c764218a909fe27c2267c`  
		Last Modified: Tue, 13 Feb 2024 01:04:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3802ad1a32f881b195f1cf878646464ede2800225f7a556a5ba3539cbbc47cc`  
		Last Modified: Tue, 13 Feb 2024 14:01:46 GMT  
		Size: 89.0 MB (88998310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16a19f3cee1fcedd6915e9948ec1e45b69558b580e977ec0a3a706d99ca4e43`  
		Last Modified: Tue, 13 Feb 2024 14:01:44 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b60c657540bdd34cade555dd30facb12f722566225e84609e42c492c6be9b2`  
		Last Modified: Tue, 13 Feb 2024 14:01:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111331c11fde2d0bd4c4ad5b8d9eaf225e0190026216183052c3241c06cb2de9`  
		Last Modified: Tue, 13 Feb 2024 14:01:44 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ff4523267719ff0cd8a5f62ad8ac13b814b6c0f09b5b32f733c45a7ba4c164`  
		Last Modified: Tue, 13 Feb 2024 14:01:45 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e567af040bdfa10cf792b6985895f426562d4b66a6b5d56da6e1c0154ca44f0`  
		Last Modified: Tue, 13 Feb 2024 14:01:45 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:bb2294982664bcfaeaa3f01c107e182b8e7cf5c67c4117fe879ec35df561c37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.3 KB (843256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0c2b5192d31da81c6967c7df0b6e908ad922f6f63a13274ebcfc0ba5b4d73c`

```dockerfile
```

-	Layers:
	-	`sha256:969b1345e85bbc3b55347960e42874824fa7cc5d66a2e0991e348b54eb202163`  
		Last Modified: Tue, 13 Feb 2024 14:01:44 GMT  
		Size: 806.2 KB (806191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1fb76836bad2505c7ab1e16881bf1a8ca70cae80fdb3d202927cab8cbf1491a`  
		Last Modified: Tue, 13 Feb 2024 14:01:44 GMT  
		Size: 37.1 KB (37065 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.18` - linux; 386

```console
$ docker pull postgres@sha256:25334b559c4c5c918d9c09d315288aa743f36dba401220d0fcf495241638da6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98407061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75926783af59370a6eac65df24ca958db7615fb663df082648d91308fdb34712`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_MAJOR=15
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_VERSION=15.6
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_SHA256=8455146ed9c69c93a57de954aead0302cafad035c2b242175d6aa1e17ebcb2fb
# Thu, 08 Feb 2024 19:40:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:40:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:40:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:40:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49393b84e7b1b8c2b5fb5da16a749eb83b146d0ab1a88c27a3215dfc328608bc`  
		Last Modified: Sat, 16 Mar 2024 00:00:47 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24982bec1f216bd78d155ffe6ada5e93622dcb6dae6abafb8475d1b3feb558f`  
		Last Modified: Sat, 16 Mar 2024 00:00:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2326672b41dcadc9cc74cb88a9fb29bcbb7c09496ed4f5ae02d6f6761b19fa89`  
		Last Modified: Sat, 16 Mar 2024 00:00:49 GMT  
		Size: 95.2 MB (95151267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b54efb4581efc943e3402b4e819f26edea7644444896b57b03885334ba53f0`  
		Last Modified: Sat, 16 Mar 2024 00:00:47 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa49bfdd24e744540094255e59e360e03832a355afeb21ce8d070023c45c8d9`  
		Last Modified: Sat, 16 Mar 2024 00:00:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662d3c8cfbc967adf6aded5ad54633b884e397480a01165733f349f0cb13e012`  
		Last Modified: Sat, 16 Mar 2024 00:00:48 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6e13a4447baa6b50efdd46d5bf6841c095dab61b44dc54fcdec2ead70512ee`  
		Last Modified: Sat, 16 Mar 2024 00:00:48 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b6107435462ad2bfaebe131a0af905d6b996fc5ffd1cf92e1c1f3409357264`  
		Last Modified: Sat, 16 Mar 2024 00:00:49 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:eafb906a69a4524ab6088bd5ca4af50222c3551307ae89f40ead6cfcd005ab46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.2 KB (993247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aef5e9258a647a74bad89a3533d96402482414b98a439ccfd922a61965870f1`

```dockerfile
```

-	Layers:
	-	`sha256:5e61a5244cdbc7ae55925bcd6fd12926a995bccf0ee4795901140b3180e37ed0`  
		Last Modified: Sat, 16 Mar 2024 00:00:47 GMT  
		Size: 956.1 KB (956053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7220f8772673456bd732e5c487d358a6188d6138871afa62a9d86462222d50b0`  
		Last Modified: Sat, 16 Mar 2024 00:00:47 GMT  
		Size: 37.2 KB (37194 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.18` - linux; ppc64le

```console
$ docker pull postgres@sha256:5599d16ef9176fc0d88c003ffba3543967d74c9a215d0d1bf0eef9d52175e879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99104230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fff68e1098c88980e37bfada931074ca8e1645d6eb5e73ac08e661b9b41fe48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_MAJOR=15
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_VERSION=15.6
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_SHA256=8455146ed9c69c93a57de954aead0302cafad035c2b242175d6aa1e17ebcb2fb
# Thu, 08 Feb 2024 19:40:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:40:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:40:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:40:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8902010b016148d7a344a816775bb68a2f2b69cf0eed5857366eb8f807cca9`  
		Last Modified: Mon, 12 Feb 2024 23:27:23 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b51baf31c38d029e4d936e367fa484733715acb0d9b9cd2b169bf5633a341b`  
		Last Modified: Mon, 12 Feb 2024 23:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80f0529857322e973a8884e5b40a3d3358a97d81e6f352c6ed4ca1b88d8f418`  
		Last Modified: Mon, 12 Feb 2024 23:37:21 GMT  
		Size: 95.7 MB (95739004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48ac6989733ca4aae6e9e123388aba891bb02d879a81781fa236db237c6f9c0`  
		Last Modified: Mon, 12 Feb 2024 23:37:18 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee86ba5f65ea1e8044b10d4f469af4990f207cd7ac1a6eae2e200b98c2eec746`  
		Last Modified: Mon, 12 Feb 2024 23:37:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9887b9ecfcbb1d60ccb3971c0baa022126aa055214187ad1ce261e980d100f`  
		Last Modified: Mon, 12 Feb 2024 23:37:18 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2771027065d0dcc52a955995156c4aca54ae0c472f9f4629c2ab621ccb53c884`  
		Last Modified: Mon, 12 Feb 2024 23:37:19 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62da5153cf1a7e4d3819869a009d5de348a61e96b2518b9e445b2c6471ff8f2e`  
		Last Modified: Mon, 12 Feb 2024 23:37:20 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:991747ba5eb0d05c156fae4a9fd11b6fe5459d1a3cb15f278665d5489330c439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.3 KB (840251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43528d25f4db2cc74a85abc3ebe2962dbe59d3460ed45cb1952883767fc74581`

```dockerfile
```

-	Layers:
	-	`sha256:a5b6f278a349d28274de963638fee49b8f1c878268894d1aa4b0c12f9a7f9adc`  
		Last Modified: Mon, 12 Feb 2024 23:37:18 GMT  
		Size: 803.2 KB (803155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:548be82bd096bef4ab24be8fcd0aa625cde27a77c3ae866755b7014a80ff0c0d`  
		Last Modified: Mon, 12 Feb 2024 23:37:18 GMT  
		Size: 37.1 KB (37096 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.18` - linux; s390x

```console
$ docker pull postgres@sha256:2882b9ad0fae66e92d1692239135ce2a221058fd242f98f8428940d4959bb102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.1 MB (95064784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b4f4920e77563487e1f5d2e247db621810f480b39c6fa7dc33e17bd651e23c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_MAJOR=15
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_VERSION=15.6
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_SHA256=8455146ed9c69c93a57de954aead0302cafad035c2b242175d6aa1e17ebcb2fb
# Thu, 08 Feb 2024 19:40:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:40:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:40:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:40:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d15f368e8218ef7346413be292e59b3a90fc69fc6c4e8e685988c0967f898f`  
		Last Modified: Tue, 13 Feb 2024 21:29:43 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c80c38641200ffd1eb7f80c02e4d0af67a4cc46b8910d8b23a01b5a777ede09`  
		Last Modified: Tue, 13 Feb 2024 21:29:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cd9c72c26a4f6aa0502f433d929a78a0880132be3ab041a11c1ed5f0300f4b`  
		Last Modified: Tue, 13 Feb 2024 22:20:45 GMT  
		Size: 91.8 MB (91830520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21ab05c1b05f20c5619957677b37fbc50de9100327a9808b3dbacfece381dbc`  
		Last Modified: Tue, 13 Feb 2024 22:20:43 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0ef90438e149e5eb471d56af7634357726b4d8cd681286cc410902cbd63fcb`  
		Last Modified: Tue, 13 Feb 2024 22:20:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ac6335ee315aa484b8ff925b9c5e14683d723b677ce6f8719b68ad9887e12d`  
		Last Modified: Tue, 13 Feb 2024 22:20:43 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2732fbd315314a32639fd36f030eaac1672fd509c6be282d033f8cbf0c87036b`  
		Last Modified: Tue, 13 Feb 2024 22:20:44 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2602e44c5ead0fac36b3ccf452e873ba1167b45a4766c5228d2c3619f107e0`  
		Last Modified: Tue, 13 Feb 2024 22:20:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:fc4fe665299a32e940efae66147e241615b70b0eae46fda18515cbba490fa3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.6 KB (841606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fba43d158a512bf74c88ba7fc6062607724b57cb1c2a0542bd46283f0203dfd`

```dockerfile
```

-	Layers:
	-	`sha256:6236d3f3aeb24029f47ee5cf1cf7a2188287eb7d28c9b7c58accce4783add2d1`  
		Last Modified: Tue, 13 Feb 2024 22:20:43 GMT  
		Size: 804.5 KB (804548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f184835a977cd026c548b7802fe023eb1341735d5b18c58b6815f4b9507adccb`  
		Last Modified: Tue, 13 Feb 2024 22:20:43 GMT  
		Size: 37.1 KB (37058 bytes)  
		MIME: application/vnd.in-toto+json
