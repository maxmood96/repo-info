## `postgres:15-alpine3.19`

```console
$ docker pull postgres@sha256:e05657f56b52cdeda9b18529389c5e60cbb87969b1777f6fa7d9ea6b49d8f0c6
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

### `postgres:15-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:96c1413ba7871a0f3480034a41aca641f0ad1f724eb50f5d8ed668a51b9b22ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94828417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555a3df232f5944f0ba21fe76ed49c731e34fd8510325d0c4cb41d3c965685fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54d40fa3899a525bbb99c32ebce8c195e7b25c87abe156b8197f8e4ef6ad486`  
		Last Modified: Sat, 16 Mar 2024 00:00:35 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bba88902c495619a79e90cd759e1e0787fcb2b941ae5afdfef06b2cc04470d`  
		Last Modified: Sat, 16 Mar 2024 00:00:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908252890a7bca20e3aae2e6f41e2db2b3176cc2beb06f2cd9a1bff45c3b374c`  
		Last Modified: Sat, 16 Mar 2024 00:00:44 GMT  
		Size: 91.4 MB (91402958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c626fde205e985bf537613af5e1812c190f5515defc01ed2234dbd85cbbb43`  
		Last Modified: Sat, 16 Mar 2024 00:00:43 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eb99bde370d181a85727cd138bdd64d6ff9fbf4ee777cd84b48c07835899f6`  
		Last Modified: Sat, 16 Mar 2024 00:00:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b7eaf1cdf2526392d9da79bca4166f8df20d980e9761a61c8081e292c2ceee`  
		Last Modified: Sat, 16 Mar 2024 00:00:43 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9195d5564e8cd5d403eb226dfc9916dc8791028c234d28511efc70150b671c`  
		Last Modified: Sat, 16 Mar 2024 00:00:44 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83e77e7f801de9c07384a17b32607c60e84a6bb4ba3d5b3220388032fb0b7fb`  
		Last Modified: Sat, 16 Mar 2024 00:00:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:7f2d5a50e805cbc221b68ebbe24cc7e291ae306ca7808ae0aea9ee50d52df84c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **995.1 KB (995150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c970c3a84affc5377b85236dc2a43b070322a0b30e9a9eb8a89cb26503d9845`

```dockerfile
```

-	Layers:
	-	`sha256:f7df861eb5e4bf356b4689260e312a2671bdf11d8b8b8dcafcd39828a5f68d4a`  
		Last Modified: Sat, 16 Mar 2024 00:00:43 GMT  
		Size: 957.3 KB (957307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e45bb11067114da20db72a15083f8fc337930ef8857f641ae3699823d954154`  
		Last Modified: Sat, 16 Mar 2024 00:00:43 GMT  
		Size: 37.8 KB (37843 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:7773647bd9b4819da937c50499e7360bb21963aab75f2bbc2be73366068c9872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93611498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310c8194aa4271f054bbdc9c6878d56a2ecaa00f8f53cfb00f82f77a1480d858`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
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
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ad518b0cf26aa61d9ca7c99a519c6a1e127fb2cec34a20ee0e078ffd31d40a`  
		Last Modified: Mon, 12 Feb 2024 22:17:21 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb22ad7323dc854410efedfb052711011a92b7f1dfad1d76944fcf85ddfa0e01`  
		Last Modified: Mon, 12 Feb 2024 22:17:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d6d6c4854e77151d4213c461c2e91d92f181d01fbaa92145a3f5799832a6c8`  
		Last Modified: Mon, 12 Feb 2024 22:24:34 GMT  
		Size: 90.4 MB (90429373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28d3f3544facdd13cc6bcb566ae68a476ab170d2ab8bc6aabe68cef5daad17f`  
		Last Modified: Mon, 12 Feb 2024 22:24:31 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f5cff24bcd9388a7cf4f416d9e0136f0a6399df0824a2947058d3f0219aeb1`  
		Last Modified: Mon, 12 Feb 2024 22:24:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b48a890c028605e4c0a6c4c079998f50fada0f64e5c2936bf20c5ccc06f0541`  
		Last Modified: Mon, 12 Feb 2024 22:24:31 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cf0f591106cfd035203eae37d642487378351e17067bb15542e03b442a0254`  
		Last Modified: Mon, 12 Feb 2024 22:24:32 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381af7d7ff2fc73d2d01928680e23126704053527da8c903043fc3bffdafdea4`  
		Last Modified: Mon, 12 Feb 2024 22:24:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:585e73e5d3484028decfa9fcbe8a71de4e57510002be2ba1d888dbded716f4be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2445293a8cb63d5c68e45f75d41c9ac97b3a3652b9e968898eb49cd85ca9ec4f`

```dockerfile
```

-	Layers:
	-	`sha256:024c128895ed01953fb6db6e3fe0989791d67b992b4dd4a8240a54f92c94027a`  
		Last Modified: Mon, 12 Feb 2024 22:24:30 GMT  
		Size: 37.6 KB (37612 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:ed61aee8e98cd10776f89fdcc1f08d9f7eff5b43ac364688876cd4626c371821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88056477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c2434a0c86cf13802f9e24b7cede0bb79dc4411732bca68ae3c775a546461c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
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
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04fac8f616621198f83a4989d82db0c9e941949e87e7f5c0b60b19218b49230`  
		Last Modified: Mon, 12 Feb 2024 23:52:42 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9fa50b5978ae8773362b63ed0f8d8a0a2136155bdc38ab7e05dfcebf9e9dab`  
		Last Modified: Mon, 12 Feb 2024 23:52:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215614aecd53fc30e5d64a583518bcae530f018e89ed1c248657c4b25756add2`  
		Last Modified: Tue, 13 Feb 2024 00:50:38 GMT  
		Size: 85.1 MB (85120842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de7f24357bd6447c614b75d3b5bff8ef51ba6d465092ff293d4ad75bcc028b0`  
		Last Modified: Tue, 13 Feb 2024 00:50:36 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b59704a4d1da93a5483eaae08de24c6bb4b45eddc86f1ade77cafc9f91a4aca`  
		Last Modified: Tue, 13 Feb 2024 00:50:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b899868e8d70727c643cacbc0966aa93ccf78cf756bf1e09525e411ed3e0f8`  
		Last Modified: Tue, 13 Feb 2024 00:50:36 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513701b801239577c8710e16ff4354ecdeffac6f1c792f72fad2e09dac777b05`  
		Last Modified: Tue, 13 Feb 2024 00:50:37 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d26c7b33a4450d10bc43ea0468155c47789b18a644c97d7e28e7493847270e`  
		Last Modified: Tue, 13 Feb 2024 00:50:37 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:c82acba803bac0468ddd598accac6c4367aa2b278757dbdc769356ecb8d2cc02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.2 KB (845180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d30e234a43524807083ae369134fd0ae16d2f5c76c0abca6210e5d2c55fe007`

```dockerfile
```

-	Layers:
	-	`sha256:e82db876304462181c56a72819d77e7e15671a671132620d80c03d763008e580`  
		Last Modified: Tue, 13 Feb 2024 00:50:36 GMT  
		Size: 807.4 KB (807353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f07b26ec7647955bf468eaf53ec817cfae304c67fc3ac8be1d8b1fc854faac4`  
		Last Modified: Tue, 13 Feb 2024 00:50:35 GMT  
		Size: 37.8 KB (37827 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:9c9ca0e12cfb87329f471f1983e538f1da63a02c68c2b649233a33e49f8b280f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93597118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5933451e4a27f5234555bbb104ec8f17daee7b6bd846490643c13c70fe0048a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
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
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9855befac3cb99a213f57d7cff6c01ac9bb63db6403f5b49c297b8e85b284362`  
		Last Modified: Tue, 13 Feb 2024 00:40:33 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45189928efa78a09b7a14fb5df6c6eff8ad7099cd14d8fa99c3ea75cbf347585`  
		Last Modified: Tue, 13 Feb 2024 00:40:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa57795fb23128d0431f2cc4e1bcc7c9dabc34c43ee9fdd79aa9e6721f854f61`  
		Last Modified: Tue, 13 Feb 2024 13:32:54 GMT  
		Size: 90.2 MB (90232672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720a86fc03762388564b2ddb8973117da0de8e37d44ff20ec6eaedc99207dd08`  
		Last Modified: Tue, 13 Feb 2024 13:32:51 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe005825a51b0592ff321deca5f38eac9a6abc3171e6481189e7261fd6b3be2`  
		Last Modified: Tue, 13 Feb 2024 13:32:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac9889495977eb60b492b365e3b5bee760f8063594f8f949803ee7dc2f03c80`  
		Last Modified: Tue, 13 Feb 2024 13:32:51 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00692d7d3685ca9191f113b2e0b35ae4fe7202c5e42e34a4b9af909b976a4494`  
		Last Modified: Tue, 13 Feb 2024 13:32:52 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f011263d51785ecd63399080ffaf67fbcec4c2ce0f1032f39a9d7376928071f3`  
		Last Modified: Tue, 13 Feb 2024 13:32:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:a1fca6a81bc8f730fc2ad7c205d88bcb3ee5509227d6d1185cba1a4522908ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.0 KB (845017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6ac0ab075ff35ae8d18f85328645ba55c6574e8d168889dff6946f442d37b3`

```dockerfile
```

-	Layers:
	-	`sha256:58a94d58011dc57d3b8b3db2692366632ddb771581858a48450693cd5616edbf`  
		Last Modified: Tue, 13 Feb 2024 13:32:51 GMT  
		Size: 807.3 KB (807328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbac6b8f501f73766391d443a54ff9713cbd3183bb982757e3cd9bdafa35e0f5`  
		Last Modified: Tue, 13 Feb 2024 13:32:51 GMT  
		Size: 37.7 KB (37689 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:97abe9babe8299c96fb143f857cd77f94ee6ca208470afbc18c570f41a8eb654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100144178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971cc5a5af08a6bbac4a695480484284caf0af7fb43ab4b52df9c3b524929c95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
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
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed57a2b88531788090fe1d797eae3d2174f39595eb136d4ea849e16f52cdee2`  
		Last Modified: Sat, 16 Mar 2024 00:00:44 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67a9c4e20b18f5202e7c919e64e8a920c8c9f58f17e9ab9eda2c1dc9561f442`  
		Last Modified: Sat, 16 Mar 2024 00:00:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae5f57857cde85b3986736a583e410bbdee59f38b77b6d286b069f63aba4308`  
		Last Modified: Sat, 16 Mar 2024 00:00:59 GMT  
		Size: 96.9 MB (96883361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5c36e5505ca5a703f45d8f23e2006a1fa1f433fc166962e06202a99a2eb89c`  
		Last Modified: Sat, 16 Mar 2024 00:00:57 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19aaf54e43a57f904cf63cb074ae24065a267d66730a8ae9001439598721a3d`  
		Last Modified: Sat, 16 Mar 2024 00:00:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15eb445d3628689fada95ccd95e5bfc0e0297c22ffdca5f1b5bd87a23ac047`  
		Last Modified: Sat, 16 Mar 2024 00:00:57 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6392efad19b109ac79f782938d4022fd790b9237addf716d3bff6c58146f1916`  
		Last Modified: Sat, 16 Mar 2024 00:00:58 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e79ed2c75668e61ff693a373c858c61f286c2415549a9d5575ad63cbe8a234`  
		Last Modified: Sat, 16 Mar 2024 00:00:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:f40385a87771dbccf78a0b65ab84933677ef259080e8a6e972552fe34c52e80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **995.1 KB (995086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3844b86497e2f982159f295a15f43c7c6e363ebe61156c3782f7f7afb0a8bf`

```dockerfile
```

-	Layers:
	-	`sha256:1fa75524fb96c51e655c1cc458ab2ded23f35d146528acde97c327ffcef6c3d5`  
		Last Modified: Sat, 16 Mar 2024 00:00:57 GMT  
		Size: 957.3 KB (957282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4542dfbf6387a55d4cbfa41d06d2e5cb6a0b6ab0b720be2183d79a77f1be16b1`  
		Last Modified: Sat, 16 Mar 2024 00:00:57 GMT  
		Size: 37.8 KB (37804 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:3f6309a94c56ebc1dcd2ee2f3efabd4fe46bbbbafda99f9a7c5516cd25918a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99445540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5470982acee32ff480ffbb009f8e9dd74c62e9111b8d597935f46821bb9414`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
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
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad450287b1da6731acbc30aae17fcadfa786da2babc8ce51fc6eca315000e31`  
		Last Modified: Mon, 12 Feb 2024 23:24:16 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a37cd9eb8f983e054e3ac505f5623aff726d75841ce8d158ba1e6913077100`  
		Last Modified: Mon, 12 Feb 2024 23:24:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f624b5976e2f21950a3e2f79c84ce3ab924908421adae0d5fcc61036194efdbd`  
		Last Modified: Mon, 12 Feb 2024 23:34:26 GMT  
		Size: 96.1 MB (96070450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbbc0bc121bb1d97f71cfdb090d0691f6b90acb277dd8b50d4a986467654e3e`  
		Last Modified: Mon, 12 Feb 2024 23:34:23 GMT  
		Size: 9.5 KB (9457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71be8d4e191883af182ad75308817ea4a92ba1104cffc83c8249df075402a1ee`  
		Last Modified: Mon, 12 Feb 2024 23:34:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3418c463348ec874a8effba85aff06912c6b104f5f60e318a1fbdf498a692b85`  
		Last Modified: Mon, 12 Feb 2024 23:34:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87528dea4b7cc53f86b1f2a2d99eb3e479215a54b01f4c05e10693885fd62e9`  
		Last Modified: Mon, 12 Feb 2024 23:34:24 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05a364ef847287f36b6f5b3fadac0065a5208dd744e012ebe89972f3ed383f2`  
		Last Modified: Mon, 12 Feb 2024 23:34:24 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:b35157cea1fd11f392f98b18653890ab1e23250d609b9a099de9850c9fce4334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.0 KB (842029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b266c99bf5c258d201af49a4f680ed48ef714ca7d4a1d289f66f6b7c26e1c21`

```dockerfile
```

-	Layers:
	-	`sha256:bc6fbfaafce6fb6333b5a4e50f0ee4f483f23d3d9cd5467122ae88fb25bb0344`  
		Last Modified: Mon, 12 Feb 2024 23:34:23 GMT  
		Size: 804.3 KB (804300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d61fa4fe43f0e93b4f6ed514aae177caa9c89f47fb0d22636a56d5ffc622d3b`  
		Last Modified: Mon, 12 Feb 2024 23:34:22 GMT  
		Size: 37.7 KB (37729 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:4d06caea24a4b3653deec6c7430ebfffdfdf6d9c2a0dc6ba30be688d09558036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103744363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9205cab594b91f68163a4962f0a6e27245535b8369acc7e965a7a3176ef24c01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
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
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b574fb7062f656c15df3e24f10aa7c2933845cca8a9782da63d431d96397af`  
		Last Modified: Tue, 13 Feb 2024 21:23:54 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e10a6d15ccba05f4410b4adddd3cd30b817458b98b69829386bb79c0badb04`  
		Last Modified: Tue, 13 Feb 2024 21:23:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1076a4295e8f90f31660061e938595b6ec5bba0f8d7b5457e649d5d4423fd143`  
		Last Modified: Tue, 13 Feb 2024 22:15:10 GMT  
		Size: 100.5 MB (100484990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd0c6f011130e3f41782e93aae9b37d3561719de13c1073d9a3f786cd202a36`  
		Last Modified: Tue, 13 Feb 2024 22:15:09 GMT  
		Size: 9.5 KB (9457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1693db3707ee05eae37d75cc3c76a6ecb16be543042ec32da902b9fdfcfed39e`  
		Last Modified: Tue, 13 Feb 2024 22:15:09 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e37374ad273f9ea3bd75a499e1dbdffebdfa0e28e18e020ff8c0de1d83a58c`  
		Last Modified: Tue, 13 Feb 2024 22:15:09 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622afefb0948d0ec17103a40c2bcb858180545de01551944a186a743b4ccd71c`  
		Last Modified: Tue, 13 Feb 2024 22:15:10 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5153be38d89883483d8c9ce94d338a0948c8755f736138ef9032eff48a3ca695`  
		Last Modified: Tue, 13 Feb 2024 22:15:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:15262715b7c3629cb309719fc0f1f87022449ca3e8d5698c292141e5f26837f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.4 KB (843365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e7a542938c899d0776dff1f40349ac0db14bd577a8fa810a7e82908e362db8`

```dockerfile
```

-	Layers:
	-	`sha256:7cc08e484db18af54d70cf723715b676b91458c6811aebae0171dc7e600c258e`  
		Last Modified: Tue, 13 Feb 2024 22:15:09 GMT  
		Size: 805.7 KB (805681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ae54df306c64fdb73cc177a0788aab746d04a4b10453d55c73df42ec0e1773`  
		Last Modified: Tue, 13 Feb 2024 22:15:08 GMT  
		Size: 37.7 KB (37684 bytes)  
		MIME: application/vnd.in-toto+json
