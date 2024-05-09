## `postgres:13-alpine3.19`

```console
$ docker pull postgres@sha256:7d4c4543cb3827a2dee4d3f4812f2550c998d14c21d13f356f8a85a523ca5cf0
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

### `postgres:13-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:8f70e7c1e0230d7ea7004f1d93757fb2a9e7505e4f93529f48b191920102acd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92678430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a010290162a34384e4f483fe74e9d0f7c2d39a3219ee5a697af748c7d2fe69c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:16:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:16:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
ENV PG_MAJOR=13
# Thu, 08 Feb 2024 19:16:28 GMT
ENV PG_VERSION=13.14
# Thu, 08 Feb 2024 19:16:28 GMT
ENV PG_SHA256=b8df078551898960bd500dc5d38a177e9905376df81fe7f2b660a1407fa6a5ed
# Thu, 08 Feb 2024 19:16:28 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:16:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:16:28 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:16:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:16:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:16:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:16:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6004f251c23733794046fc21657b2899e15e39950152d95cd878a0641f0c031`  
		Last Modified: Sat, 16 Mar 2024 00:00:29 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec102136b127f8195c5f22d8a0ced131459389c4199e2c510e89b1046cb21a17`  
		Last Modified: Sat, 16 Mar 2024 00:00:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc3135a4e30117b7c58d5515773a4124cb86dc4f84e7adcf3573c38746073de`  
		Last Modified: Sat, 16 Mar 2024 00:00:32 GMT  
		Size: 89.3 MB (89253395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a265ae010a38ff1fe22243709124ac18dc4835cd6382c76fe63039c02f87c1`  
		Last Modified: Sat, 16 Mar 2024 00:00:30 GMT  
		Size: 9.0 KB (9020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67eb691b206cce611d1ace22d962f893128d2bc92a17b69a91ac0cddf9f7ecfa`  
		Last Modified: Sat, 16 Mar 2024 00:00:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67622a701b6ad73a5f3ef46b000bfc90a4c8cac6f41d13428220142fe029a351`  
		Last Modified: Sat, 16 Mar 2024 00:00:31 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb2402d1f597a89a593d8767e43dd2c24a2d289019d983a4bec652eed3445e4`  
		Last Modified: Sat, 16 Mar 2024 00:00:31 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c064158f0d5f901222fd82eedf9e60fecfc2b61111db2a82a088888615c142`  
		Last Modified: Sat, 16 Mar 2024 00:00:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:b8cf2c08e95d2395be5e5b081886581df2c37de1ff609000a9a0efb184738495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.9 KB (991905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8c6df3f22065d42316ca05a48706aa257e78107ee5a05cd3850039c60afcd6`

```dockerfile
```

-	Layers:
	-	`sha256:4170ed78663e704dade949eb9a7a5f049a806798f02112b4e7f0d59a685bccca`  
		Last Modified: Sat, 16 Mar 2024 00:00:30 GMT  
		Size: 954.7 KB (954651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d56b234bd7c115415d547c6637f925e5f6b5720ec1b1d36f7a0d90aefed6843f`  
		Last Modified: Sat, 16 Mar 2024 00:00:30 GMT  
		Size: 37.3 KB (37254 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:c48a74b14fa8b900235d9f192d6d905f03adf2b587450c27e290b722c4ba694e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93241439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac8ad09979054f85650876feee86a75d30395394e8203cbe1acb6ca12b85dd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_SHA256=42edd415446d33b8c242be76d1ad057531b2264b2e86939339b7075c6e4ec925
# Thu, 09 May 2024 18:16:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b675d45afe983b29c7135f33138e534ba9aca9ca6d05d28e546e09d1e6bba8`  
		Last Modified: Thu, 09 May 2024 21:59:43 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4f6c09ac2d383e82b8fba12dd71c915fd20ddea25bd838ee27c29df1a0982d`  
		Last Modified: Thu, 09 May 2024 21:59:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b818a51c601f5b72f0cb7eeb232fa6455e258453812de07a82b00225be9b4c2`  
		Last Modified: Thu, 09 May 2024 22:19:46 GMT  
		Size: 90.1 MB (90059761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8892fe3a3699774b7c5cbfe4ac1c19bc6eec2782a60d9112e99e65bde182bee4`  
		Last Modified: Thu, 09 May 2024 22:19:44 GMT  
		Size: 9.0 KB (9009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b492741a1d31c401cb9fa7fc6c5cb97b1c403fc745083cd0446b8745d905ed22`  
		Last Modified: Thu, 09 May 2024 22:19:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8c76eb38f97574e351e8964de87a001548e44e5c785aa3aa1e569aa75e4c0c`  
		Last Modified: Thu, 09 May 2024 22:19:44 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28651b5702a54dc8bb04330718f96596b337c52594f671108d1d3d3836db0606`  
		Last Modified: Thu, 09 May 2024 22:19:45 GMT  
		Size: 5.4 KB (5412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c62240f9551f90efef85a98d26310a6ad05a1c19e0b2c5141ecbb8f58dfe30`  
		Last Modified: Thu, 09 May 2024 22:19:45 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:63d2d82a57134149227dcb47d188d0b84257b5239613c435f7cfdd475a0c4797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 KB (37021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c794f7ed89b3d6e5fb9f512f14824e2c13db46cc3133b8f11179e5772bd6c0b8`

```dockerfile
```

-	Layers:
	-	`sha256:f47f5b1366ed5240a79fc885785f67a1dcc9ab5c8b98fe0fee7328efe3f5ea40`  
		Last Modified: Thu, 09 May 2024 22:19:44 GMT  
		Size: 37.0 KB (37021 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:2d360ddf9cd707233115f42dc2d16db155e635d7fd611af354a816e6f0c07f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (85995997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087103d4f7b471664cf8ee5d2804223cf1dad329cd75ceac2aad08c202492611`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:16:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:16:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
ENV PG_MAJOR=13
# Thu, 08 Feb 2024 19:16:28 GMT
ENV PG_VERSION=13.14
# Thu, 08 Feb 2024 19:16:28 GMT
ENV PG_SHA256=b8df078551898960bd500dc5d38a177e9905376df81fe7f2b660a1407fa6a5ed
# Thu, 08 Feb 2024 19:16:28 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:16:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:16:28 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:16:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:16:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:16:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:16:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34183be10276d5bf28456f8dfa0b74b7d3728c5cf15e6e32a1203d02c80f06ed`  
		Last Modified: Sat, 16 Mar 2024 16:21:42 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bfc51b527ab2c0a5829fb7c7ccd2555218ae3b9c54fce2f19c92a88f06ebe1`  
		Last Modified: Sat, 16 Mar 2024 16:21:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fea1c6335af6ab1e2868bb1c33418ed43373a90afed801156f159a1a205eed`  
		Last Modified: Sat, 16 Mar 2024 16:54:10 GMT  
		Size: 83.1 MB (83060787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08970eddda7ce59e2cd900ec909375c25b2f63844b993f849c1ca67b717be352`  
		Last Modified: Sat, 16 Mar 2024 16:54:07 GMT  
		Size: 9.0 KB (9025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc009420560be947efe7891071e8562ab4c5ee3d6b316af0493b3ee6645d69f`  
		Last Modified: Sat, 16 Mar 2024 16:54:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11a8a412173d0e33ed9fd68ffb1fee1c45f8c7f9f62af3e09063eda0ecaa49e`  
		Last Modified: Sat, 16 Mar 2024 16:54:07 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93954aaed5893d6b8791ee999da66900da4672393b65341c978057546e49bc4`  
		Last Modified: Sat, 16 Mar 2024 16:54:08 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25b7b8314a8fc8d56417bd36d25b7d1a449a36f5837589233f1bb6615c887d4`  
		Last Modified: Sat, 16 Mar 2024 16:54:08 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:118705a611a06c145d9527b7b1763a254d0716a94f9727e4fc634d1b4c4a9d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.9 KB (991923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0cce825eb76f7d5cf21e4d081a1715aeb2955f46c28bd4656283cbd4ffdf3a`

```dockerfile
```

-	Layers:
	-	`sha256:6e2acc41c2a472ac9678a11a89cd21d40215d894dc06da8f593b6a8a4631b636`  
		Last Modified: Sat, 16 Mar 2024 16:54:08 GMT  
		Size: 954.7 KB (954687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1317382518ef77c32114c50233fb165b5f5f47a3f20c8be70a3f7b6e34ed2461`  
		Last Modified: Sat, 16 Mar 2024 16:54:07 GMT  
		Size: 37.2 KB (37236 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:86d416a700dc23cc9b4975afae5f0388fd5ca2d5b5e68141f3139e93a2628f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91468770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dcd1d8e16bc33e35409ee87885af1c65f2d5352d11b7602fcfdfce0b7b6b133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:16:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:16:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
ENV PG_MAJOR=13
# Thu, 08 Feb 2024 19:16:28 GMT
ENV PG_VERSION=13.14
# Thu, 08 Feb 2024 19:16:28 GMT
ENV PG_SHA256=b8df078551898960bd500dc5d38a177e9905376df81fe7f2b660a1407fa6a5ed
# Thu, 08 Feb 2024 19:16:28 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:16:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:16:28 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:16:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:16:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:16:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:16:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73755f5e6a3e2578f900066d181e75490b8bf689b8d0355238deaed61e3f05c4`  
		Last Modified: Sat, 16 Mar 2024 15:59:53 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a60b4a71875ce3dfc2287bf071788323b63279c8053af79546e71be4447ba4c`  
		Last Modified: Sat, 16 Mar 2024 15:59:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5976ae9a0fa62145eae6c304b54d7d0b08e6006a6c05cf0b12ac519bf791f6`  
		Last Modified: Sat, 16 Mar 2024 16:26:26 GMT  
		Size: 88.1 MB (88104752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361be1980cf0d3d039541289164f2bbc6af8060eecbcf6dfe34b623324894b08`  
		Last Modified: Sat, 16 Mar 2024 16:26:24 GMT  
		Size: 9.0 KB (9021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2cc6916eaf873241f08f899a103ad8b3b6d0be5bd0bc35bc0356cec1b12521`  
		Last Modified: Sat, 16 Mar 2024 16:26:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e4f47ec03c5396a8984827cbfb9fb62a9cf515215c7a40d3663f2f8245de89`  
		Last Modified: Sat, 16 Mar 2024 16:26:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14fb22ba4ce35877a59f944a7efdc3f0b289903a0d10d3fa9158585ff0d82af`  
		Last Modified: Sat, 16 Mar 2024 16:26:25 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0279729c0a371e10a4b5a62d259ff8c71623bda7e532b5db07108c0d61e89d27`  
		Last Modified: Sat, 16 Mar 2024 16:26:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:3af816241ac0dca1406caea2e90217e8d4b9714735d0475cc9cfa2ec0c0a9b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.8 KB (991760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093be1600674b2fa30e4600064a491b7ee85643b98c09cc631f2019c227d6c3d`

```dockerfile
```

-	Layers:
	-	`sha256:aff84f9cadefde58bd9df3b78a63b9d5461a3fdd8efebf0568d520db1a0df668`  
		Last Modified: Sat, 16 Mar 2024 16:26:24 GMT  
		Size: 954.7 KB (954662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcbd21fb05cac8c79c8a264c0112f029622f7ce63f894500da518f4a79af15f3`  
		Last Modified: Sat, 16 Mar 2024 16:26:23 GMT  
		Size: 37.1 KB (37098 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:20d72d86afa95a20e662c931463b93401e552096cccf700fd5266af6127b1389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99814188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7570519eb35269c5b89b6b1933d894797c8732b3d1598747831608c27853fe4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_SHA256=42edd415446d33b8c242be76d1ad057531b2264b2e86939339b7075c6e4ec925
# Thu, 09 May 2024 18:16:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d51dcea02c7e4bce15ce2497d477899e40491a5699bf6222943c25a3d3dd83`  
		Last Modified: Thu, 09 May 2024 21:57:05 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7e50cbdc7c01e0da3f1a672326aabb89ffe278e48e80c6653806632f4a5831`  
		Last Modified: Thu, 09 May 2024 21:56:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106f53067ede9bc04a0a93ff4362077fbb32bda804ca4c01b07183d1eabfeb5b`  
		Last Modified: Thu, 09 May 2024 21:57:08 GMT  
		Size: 96.6 MB (96553807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9894f9e6e693dcaab43ed707fdb005dbb9759d478815ca05c2ee4c4d93b380`  
		Last Modified: Thu, 09 May 2024 21:57:05 GMT  
		Size: 9.0 KB (9012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7610ca085e65ef4fa720b7b2d2998ca624fb28b185eed29b5da9c62193c2c9d`  
		Last Modified: Thu, 09 May 2024 21:57:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94192920e07c903a79496344623ac874bf9f9d80af26784fa2380b075b11846e`  
		Last Modified: Thu, 09 May 2024 21:57:06 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170ed71bcb77788c26b7045782b862d14510d4465aaad370c03285df79b4b685`  
		Last Modified: Thu, 09 May 2024 21:57:06 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a715747cfda73a4f4eb1a936078cbd2625a1dfaa1bc516696ddfbda86b7dc505`  
		Last Modified: Thu, 09 May 2024 21:57:06 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:fd3c9ff5ca924b09732d698561f7f8c465b3d458c58e9b217778968545d1e916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.8 KB (991846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40eb4a167b3fa245ebd401de2ee75ab66dff2a6dfabf58f85fd104bd34836cb`

```dockerfile
```

-	Layers:
	-	`sha256:75584fbca54ae08a4f233e18cd721b4a5e6edd67ab11840724e3906132c2044e`  
		Last Modified: Thu, 09 May 2024 21:57:05 GMT  
		Size: 954.6 KB (954630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d2951b91cdff9f49d2ac60f7c866aa90fd903646dd2809eaae7024c795f016f`  
		Last Modified: Thu, 09 May 2024 21:57:05 GMT  
		Size: 37.2 KB (37216 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:421bbf979960bd6b78372d1f48a3148af5031c7d3ff25ffd94c090bf923ab61b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97121659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a650bd7abc332e687a8617bbbd626de4e4a84bd43e37ca3be59039cc3e677d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:16:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:16:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
ENV PG_MAJOR=13
# Thu, 08 Feb 2024 19:16:28 GMT
ENV PG_VERSION=13.14
# Thu, 08 Feb 2024 19:16:28 GMT
ENV PG_SHA256=b8df078551898960bd500dc5d38a177e9905376df81fe7f2b660a1407fa6a5ed
# Thu, 08 Feb 2024 19:16:28 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:16:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:16:28 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:16:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:16:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:16:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:16:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:16:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79df8127be221428a326f357e04f1c6c7907b2ac1145408ba7f22a36fe89ce2`  
		Last Modified: Sat, 16 Mar 2024 10:37:24 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e0b43ea44af8adfb383299b0e1e2f4fdbb58b567f44792024513de6b0a73dd`  
		Last Modified: Sat, 16 Mar 2024 10:37:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80e5cc5a8895d2f70140b644855b9266bd794dfe8d52070f7c1f20ba02aca22`  
		Last Modified: Sat, 16 Mar 2024 11:08:23 GMT  
		Size: 93.7 MB (93746998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836b6749480e30a565cd120e80445ae45d44dc88119a42affac38f121a472c4d`  
		Last Modified: Sat, 16 Mar 2024 11:08:20 GMT  
		Size: 9.0 KB (9027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9542fc28ab2a6416f9ab830e826f726b3502825d00b684f0c20e565193067697`  
		Last Modified: Sat, 16 Mar 2024 11:08:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec2da815cba24772d46da062135d30d5a1b58c0927fd2e1a2af4d531e98dc37`  
		Last Modified: Sat, 16 Mar 2024 11:08:20 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455539afdc8fec18655969908cce0076edf05f8f9c50e364cc66e8aec735f3be`  
		Last Modified: Sat, 16 Mar 2024 11:08:21 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce85f5f6b022eda47dacd237ab08c6f26240a38921dbf074724f20e76b24f3d7`  
		Last Modified: Sat, 16 Mar 2024 11:08:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:690d05e339cf460a85b3d7748b87b14b9d1cc6d59c7893e83988f078a4a36e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **988.3 KB (988348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e88b733932381403030eb7d266c0e14c09dcd73fb7244d16077d7b611cfbc9c`

```dockerfile
```

-	Layers:
	-	`sha256:706f02d588ca1ea0829f63e3ac8cef6b19c89791d00ad99bf16cb02d5a025842`  
		Last Modified: Sat, 16 Mar 2024 11:08:21 GMT  
		Size: 951.2 KB (951210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93e7cfb565439ec3cdd10f658c13be93e9be68e2cf488979a3c831a1e019e68b`  
		Last Modified: Sat, 16 Mar 2024 11:08:20 GMT  
		Size: 37.1 KB (37138 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:e01a880b1bfecc8bfe92662f494ca3f9a0c02ac642d1381ae03c311bcf20db34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103310235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65fcf16573961f8b30a704109fd43cf39d694293a0a4160dcd3a8242664be622`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_SHA256=42edd415446d33b8c242be76d1ad057531b2264b2e86939339b7075c6e4ec925
# Thu, 09 May 2024 18:16:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5640c2be82ac04ba5ddac695379fa624aa02fd3579b534fff1c3dd4eba189313`  
		Last Modified: Thu, 09 May 2024 22:13:40 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85541a3a0f2695e7b89ffb03367e1f86a74f6ff41d24e68ce35f629a057ca65a`  
		Last Modified: Thu, 09 May 2024 22:13:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dd03092c151047eebd5bb237c62e0e7ffd2bfe38eb77b1cb56f4274331c6df`  
		Last Modified: Thu, 09 May 2024 22:46:38 GMT  
		Size: 100.1 MB (100051299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3963917f0db58ac6d546241e396ba56e1b75bfe560eef544556217415a3f360c`  
		Last Modified: Thu, 09 May 2024 22:46:35 GMT  
		Size: 9.0 KB (9019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91ff4b1233cae83bdca107f26773c84fc286fb266fb551e3408567e7738bb72`  
		Last Modified: Thu, 09 May 2024 22:46:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d924cbf41252f0d2c8a2ce101c520806e51d2a705bfd191868d8c460fc83c66`  
		Last Modified: Thu, 09 May 2024 22:46:36 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2082434feba5014a5e736011e1da03331d405932bfb111eea3a82db1bbc80de2`  
		Last Modified: Thu, 09 May 2024 22:46:37 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d339372229977abb4ba645677ec4285ad57f756e58bb3ab528ce7368ece21bad`  
		Last Modified: Thu, 09 May 2024 22:46:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:a99b50b8126578110762a67679bc147ca362c3a7d1631e770254cfd5517d3088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **989.8 KB (989797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271e8259b0499c6b85288fc54cad3cc6f6caba372174634c168e7c431a17158a`

```dockerfile
```

-	Layers:
	-	`sha256:f0bbcd70a8e8ad9abb7c4006f175e32208e23cda91dd835b36ed2609e320d58d`  
		Last Modified: Thu, 09 May 2024 22:46:35 GMT  
		Size: 952.7 KB (952701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67ba99ecaa910a77f901b98c81b7b16313d7498ab2bbc519e5c1ad270425e8cb`  
		Last Modified: Thu, 09 May 2024 22:46:35 GMT  
		Size: 37.1 KB (37096 bytes)  
		MIME: application/vnd.in-toto+json
