## `postgres:12-alpine3.18`

```console
$ docker pull postgres@sha256:260970ad77430aad46e073235428c7442687b65468807e70e72ef47f380162b1
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

### `postgres:12-alpine3.18` - linux; amd64

```console
$ docker pull postgres@sha256:6e74033958f3acd0502375f84cdf9a1b07fee268817de7b6536bafaa7354316e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90531754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506a62efbbf09f53d331cac6d6d0447b4fc79cabf1ed46a9eb3a5d2482690192`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_MAJOR=12
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_VERSION=12.18
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_SHA256=4f9919725d941ce9868e07fe1ed1d3a86748599b483386547583928b74c3918a
# Thu, 08 Feb 2024 19:02:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d314cfab9d9de21dd7e1aff266a9b7dffb6a6af3bd9468981d7b7bcdfe477`  
		Last Modified: Mon, 12 Feb 2024 21:59:46 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619095e9b0ea945dca68c94eb502f132d8aa93279ba7440cccc367f69cc4c3e6`  
		Last Modified: Mon, 12 Feb 2024 21:56:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5069b026ef8c5e16d7e5c69ebfbc0e851589f66e363af734b2abe6abdd35ab10`  
		Last Modified: Mon, 12 Feb 2024 21:59:48 GMT  
		Size: 87.1 MB (87113236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7626b775d8246b217b18ca855a02e6b91913d0fd24ffbfbca2a1eefa377a64aa`  
		Last Modified: Mon, 12 Feb 2024 21:59:46 GMT  
		Size: 8.7 KB (8691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8a7f2a128bbac0d225611f2c0636718c4fe3c43c08a5fc0701c63e8b8a2e52`  
		Last Modified: Mon, 12 Feb 2024 21:59:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eab6a92474d64bfe4d78d855e9d4939184782c12325e0e6fc4c5aec1735f7d0`  
		Last Modified: Mon, 12 Feb 2024 21:59:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfefd002830994d532e3446fabcc5684191bf64a53680f327c869c9cbe08773`  
		Last Modified: Mon, 12 Feb 2024 21:59:47 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a907eed4e8a3b554503e80b30b247e39ccbe7f9c94f089fd0e518cee7004f3`  
		Last Modified: Mon, 12 Feb 2024 21:59:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:7433e4023fed33f83c3c4685f376cb1240ca98e775df3daf65057d9e62f18d06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.3 KB (840264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44eff0864c95fea327c6e9ec8191a48c968fd6dda6e01f3848575b1227102a7`

```dockerfile
```

-	Layers:
	-	`sha256:58d6d0e2aa1a4eb75b9c096af344d29308bcb2adf735dc91f548681332616761`  
		Last Modified: Mon, 12 Feb 2024 21:59:46 GMT  
		Size: 803.6 KB (803632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1232e7967d270ed2cab05f0e1192f0abc148d496143519bf053e803e5cd98a6f`  
		Last Modified: Mon, 12 Feb 2024 21:59:46 GMT  
		Size: 36.6 KB (36632 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.18` - linux; arm variant v6

```console
$ docker pull postgres@sha256:d12aed4da21e59dfdf6de0de64316e5fa63cf13b8cf4ff30d7838cfb69ee66b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89346670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035981b01e7f40f5928c0e8a0d3f8077551bfcfa1ae0ee0128f7f434c574d153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_MAJOR=12
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_VERSION=12.18
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_SHA256=4f9919725d941ce9868e07fe1ed1d3a86748599b483386547583928b74c3918a
# Thu, 08 Feb 2024 19:02:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:02:23 GMT
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
	-	`sha256:2337b5a2dde23a2492a02094d4ac41f2b89543feef95c3567b838e2864eb9dc9`  
		Last Modified: Mon, 12 Feb 2024 22:48:41 GMT  
		Size: 86.2 MB (86183631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6b0478657592a8298cfb6718f18d3f7710024a9c33a32b18772d08db25fbac`  
		Last Modified: Mon, 12 Feb 2024 22:48:38 GMT  
		Size: 8.7 KB (8696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3d9e878fa896f77e9d21884fd2dc9e127a16ebe0126bd85a0e3da59a514760`  
		Last Modified: Mon, 12 Feb 2024 22:48:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f09a57e1306e067020a0e03103760dd58223e8a4cdd0659b5b2799e676611d`  
		Last Modified: Mon, 12 Feb 2024 22:48:38 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442c2f0704af37d3256031f75ea9926d66f2b0236b60e26870de3855de223bd1`  
		Last Modified: Mon, 12 Feb 2024 22:48:39 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1074d89240bb124b8ba96d9f7a580c0dfdd57ce1f1809cda3b20389a695119c5`  
		Last Modified: Mon, 12 Feb 2024 22:48:39 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:5f4257c9d583565b3027e212eb8ac16cc9f72d7c2e429d9c96fe5e29a5dcac8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb41fdb2b7d74f2a70558a1391ba7ac438a3d859805e321e336a5d480339ed7`

```dockerfile
```

-	Layers:
	-	`sha256:bd1ccce29fa1bc0edb367f24c306267ad2fe41d1784acbedf56100e6ff25192f`  
		Last Modified: Mon, 12 Feb 2024 22:48:38 GMT  
		Size: 36.4 KB (36383 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.18` - linux; arm variant v7

```console
$ docker pull postgres@sha256:83114bebdcb3f5cb45f4cc6d370d27d929114402ac37c2a4243ba2ec0ef9b81d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84099557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48493eb42a294c1becfd2e25cc90220e77fcd4e882f16cc149f17965cda6502`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_MAJOR=12
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_VERSION=12.18
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_SHA256=4f9919725d941ce9868e07fe1ed1d3a86748599b483386547583928b74c3918a
# Thu, 08 Feb 2024 19:02:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:02:23 GMT
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
	-	`sha256:90bd9caba56d5eff40730e102e95acef5f49178f2d84ab0b3cba6966b132a580`  
		Last Modified: Wed, 14 Feb 2024 00:43:40 GMT  
		Size: 81.2 MB (81182200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1c2027167f9239f8f2e924f805f4f36d0abb1ad9dde9ed1df7ae9017590419`  
		Last Modified: Wed, 14 Feb 2024 00:43:38 GMT  
		Size: 8.7 KB (8686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8fe857c8283233de643bbb33d87155ad56d25368c1575f51c6e8cfae5f0f32`  
		Last Modified: Wed, 14 Feb 2024 00:43:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f63695491669c9bb8c01d935bf91ebf6880fab1a80cfadef102d1597efdef46`  
		Last Modified: Wed, 14 Feb 2024 00:43:38 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ad104af9ffb99886cbcf2f21a0f1f9551059256ccb9336eafa72b6efb0e0af`  
		Last Modified: Wed, 14 Feb 2024 00:43:39 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76b6b628e91a0c1d2063421ff7f7183f5dda689d64aabba1ffea82389cc7bc9`  
		Last Modified: Wed, 14 Feb 2024 00:43:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:2b0b93481eefa722b6b31dbc30e51d0ed3060654d9c5d25c13e76bb29194d6c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.2 KB (840250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695afa9b22fcfd5507a8febf00aa0a6bc1adaeae1590ce7da0d1c41602354862`

```dockerfile
```

-	Layers:
	-	`sha256:1c9273e535737cce677904376db3082cd354e7071a1250fc0b9f3277ded8b246`  
		Last Modified: Wed, 14 Feb 2024 00:43:38 GMT  
		Size: 803.7 KB (803652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3054ac759b7610a77d9ada7de362b2d76474c9522778e0934cfeb9e157b10ab`  
		Last Modified: Wed, 14 Feb 2024 00:43:38 GMT  
		Size: 36.6 KB (36598 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:7b82b9af1c878d712796029605a358341cdac37556eec7213e2d77ac1d1ff66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89583448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ad20167f64ca4a53eddb38c4983bab7ba264aac8fd60d6788cdc07fbfbd912`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_MAJOR=12
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_VERSION=12.18
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_SHA256=4f9919725d941ce9868e07fe1ed1d3a86748599b483386547583928b74c3918a
# Thu, 08 Feb 2024 19:02:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:02:23 GMT
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
	-	`sha256:552879be84beeaef6d06d5d9738f11141101f8adf5b8e60d0b4e2462d494d412`  
		Last Modified: Tue, 13 Feb 2024 14:53:11 GMT  
		Size: 86.2 MB (86234119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8cf5a2d8a4d88001bd73e22d332900ef08373c01c8a6f889a5b26a1792be7e`  
		Last Modified: Tue, 13 Feb 2024 14:53:08 GMT  
		Size: 8.7 KB (8689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45b8f025221f752a1e2df58e36ac2bc1698c6f9fa8cf5d27ff9ad311476ebf2`  
		Last Modified: Tue, 13 Feb 2024 14:53:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13e44737d03b5adbbb5cd2032ef3ef8e5c845fc069bcc35a82bdeb923c9e893`  
		Last Modified: Tue, 13 Feb 2024 14:53:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45afb69669ec8ab96e151b7bef6f8e92b7b1d0cb08c98cec81fc024925d2128`  
		Last Modified: Tue, 13 Feb 2024 14:53:09 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1b4c609ac5e618713f900a19e9c4971c75222dd342f53c2bd1992e4487e382`  
		Last Modified: Tue, 13 Feb 2024 14:53:09 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:ae02d49ff80498683d086e0d0ef649c2b4592526fd946f9d82fc3ae2ab6e9a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.1 KB (840110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1743b166aaa030c67ad5d6b85bd249474202435fa17dd72144352ca3adfb6b0`

```dockerfile
```

-	Layers:
	-	`sha256:dc1ad33ed5784ecc243b2e84a3ecaa9facd0bfa4f31cd7fd605aa47a9f9e9626`  
		Last Modified: Tue, 13 Feb 2024 14:53:09 GMT  
		Size: 803.6 KB (803639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58756d4fcf59a45047fd6542605387329977d92165da1bd27a14691188ee210d`  
		Last Modified: Tue, 13 Feb 2024 14:53:08 GMT  
		Size: 36.5 KB (36471 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.18` - linux; 386

```console
$ docker pull postgres@sha256:35a3d7d2b54b57dec6d008018f0886af098dbc7c9db2174849699a05e66cfec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95459043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cc4b5a9641eb01443dd3d90f44e6a6cd5679ccef3dc35be5fc49abbf71267e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_MAJOR=12
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_VERSION=12.18
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_SHA256=4f9919725d941ce9868e07fe1ed1d3a86748599b483386547583928b74c3918a
# Thu, 08 Feb 2024 19:02:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:02:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25853929606d7e45c2eed1490d4930b1403451cfac0324b6e97d0b6aa6cbaa`  
		Last Modified: Mon, 12 Feb 2024 22:00:06 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbfa21fa1f90f6df886867978673983f9134c2b54a37d9ba3658efaaee205809`  
		Last Modified: Mon, 12 Feb 2024 22:00:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a961f1dff885739e01c488d85d6770bc59dd2773fb7c7653d44c3abf9066ee5`  
		Last Modified: Mon, 12 Feb 2024 22:00:08 GMT  
		Size: 92.2 MB (92204007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32004681e46c8f163c582cc36be4e1706377542439b5f3e94c7301cddf6b07d`  
		Last Modified: Mon, 12 Feb 2024 22:00:06 GMT  
		Size: 8.7 KB (8687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa731687e6f1a6b70900345812fe97823f6991e2a836c0bd4ed1c8aaa005896d`  
		Last Modified: Mon, 12 Feb 2024 22:00:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bd971e6aec186c363293239edf2d4ad8439f2e315716d08a394f22e481175f`  
		Last Modified: Mon, 12 Feb 2024 22:00:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69fbf023599a72f3bd07a27819e87a8bc1f60551058d5699bf12248a4776182`  
		Last Modified: Mon, 12 Feb 2024 22:00:07 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd588517ca1c34edbd2627ac4e8f207591cd3f551857dc33fcef90181eedff27`  
		Last Modified: Mon, 12 Feb 2024 22:00:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:e26dfe938a263ed2ede7401f0ed4c045f4260df3db2dfe8924f3c712063f658e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.2 KB (840218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c93e51e5293c8b46095ff706ee268e2646b17f7f27d1e2375d92beb2e8fb310`

```dockerfile
```

-	Layers:
	-	`sha256:b53bfa067479be097a7c483f89fb8ce2136e9695448ff7dce756dbb18a38e6b0`  
		Last Modified: Mon, 12 Feb 2024 22:00:06 GMT  
		Size: 803.6 KB (803617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d07ff3c06f9b48b1b161c70582cc11bb22bfbba7ac032047edcad24ed260fd42`  
		Last Modified: Mon, 12 Feb 2024 22:00:06 GMT  
		Size: 36.6 KB (36601 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.18` - linux; ppc64le

```console
$ docker pull postgres@sha256:64142d1041fc29d04b33f79ffc26de0d5d077a37173a959788a9595e34529492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96061394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b4f7a97d33d5c9197c9ea7f1bf5cde415611c30ead5f75e67a6f08a9d58f1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_MAJOR=12
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_VERSION=12.18
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_SHA256=4f9919725d941ce9868e07fe1ed1d3a86748599b483386547583928b74c3918a
# Thu, 08 Feb 2024 19:02:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:02:23 GMT
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
	-	`sha256:84ec5238811f805c5b6efe0398e9ab84173c4ad3d002c92afbd3777695026cc3`  
		Last Modified: Tue, 13 Feb 2024 00:29:23 GMT  
		Size: 92.7 MB (92696924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fa84f2926a8a74f8300621e7b99353cc9b4b4cedfb990c8ddd555ae3e7d0af`  
		Last Modified: Tue, 13 Feb 2024 00:29:20 GMT  
		Size: 8.7 KB (8697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9490db9eb3d055320456133b651d0c8dd0bcb5a26c69cdde6647bc90d8c481`  
		Last Modified: Tue, 13 Feb 2024 00:29:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f2f36db389ad6b76ba73c03fdd1c8a10e1fb288e40068fad229e2e8fe38046`  
		Last Modified: Tue, 13 Feb 2024 00:29:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a32b171b2ec22e46bee31e8d3284d3a140a456d6ca5d2d05c9af9d4c94ff4e`  
		Last Modified: Tue, 13 Feb 2024 00:29:21 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7bac01d0bf49e69a9fc5f7e88650fa485a6d594eca014d43cd75ac14e8767b`  
		Last Modified: Tue, 13 Feb 2024 00:29:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:7576967a9acb86f2b1eaa246f5e5e0361190d55683220ff2db4a497130ac018b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.1 KB (837106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41177abfe8607bd0fc51b131cbc8c0a52257f4caf9b4f23c7dd893821c7ed113`

```dockerfile
```

-	Layers:
	-	`sha256:5d1cc99d8e8ef17924044a8294c7d170288ac42292ec2312030c853ddb7b095e`  
		Last Modified: Tue, 13 Feb 2024 00:29:20 GMT  
		Size: 800.6 KB (800603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f75c120edef99e6626fae2485709227c14264d1c09585b09e1059708f15a345`  
		Last Modified: Tue, 13 Feb 2024 00:29:20 GMT  
		Size: 36.5 KB (36503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.18` - linux; s390x

```console
$ docker pull postgres@sha256:f15c10d92cc9f172e22f2edfcbc01147dfaba375ed5312f106b6d18843ebbe5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92115779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1bae0bb92538352efc8c7f3c921d14ef1afb1c9bfffa7a974791e4806fdc1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_MAJOR=12
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_VERSION=12.18
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PG_SHA256=4f9919725d941ce9868e07fe1ed1d3a86748599b483386547583928b74c3918a
# Thu, 08 Feb 2024 19:02:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:02:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:02:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:02:23 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:02:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:02:23 GMT
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
	-	`sha256:1fc98ababe85953903629b2b191169af9edb62b7e51305a8fd7074b093fefbfe`  
		Last Modified: Wed, 14 Feb 2024 00:14:05 GMT  
		Size: 88.9 MB (88882279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca31e58c33d0d414e60e6e2bbd9602993c3cafc6cebd4e522063133b4b34f74`  
		Last Modified: Wed, 14 Feb 2024 00:14:03 GMT  
		Size: 8.7 KB (8691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127acfea4df5a36989c3d869ba9cbd325d56ba6386913d48aba562b558339592`  
		Last Modified: Wed, 14 Feb 2024 00:14:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a81a7dde2362db22975d941327c09e1e3f6faef23d52690886e2a7514c4a55b`  
		Last Modified: Wed, 14 Feb 2024 00:14:03 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486364e2b519ffe1f2c54abd2a93908febfb8aa67bd7ca8a06321e9394204ae6`  
		Last Modified: Wed, 14 Feb 2024 00:14:04 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afab7186de968e3f06a8223f8a4a34403ba3cbd832278613d3bc19faac4dc2e5`  
		Last Modified: Wed, 14 Feb 2024 00:14:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:1b9e95582d13e0f167af3ccec5b43a5be70df1060d28c88223178413529e4a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.5 KB (838462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d98d0f4c4b5cc127ec5d3aa9f816a0be139a292c291bdafe0356872976ba070`

```dockerfile
```

-	Layers:
	-	`sha256:54816957a7511cdae7b661b2dd8989eb1c8da319a0f2d2ed1b0b353b92f74281`  
		Last Modified: Wed, 14 Feb 2024 00:14:03 GMT  
		Size: 802.0 KB (801996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c4a71528efd52f10435bcc0b64410eff90d569ba635fcda2452d349e3b4956`  
		Last Modified: Wed, 14 Feb 2024 00:14:03 GMT  
		Size: 36.5 KB (36466 bytes)  
		MIME: application/vnd.in-toto+json
