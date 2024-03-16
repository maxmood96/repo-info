## `postgres:13-alpine3.18`

```console
$ docker pull postgres@sha256:c064de6bc1f176b4b8b2a4ecea514a85b96bf502e7074ff446f2ac638698f456
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

### `postgres:13-alpine3.18` - linux; amd64

```console
$ docker pull postgres@sha256:588167d2551434be8bf8b0b3c33df13efcdb4f52ba37031632b91d1dc5638d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91254397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ecb4f2d6eacc8426fb8844f6b62e69f2b7ef566b0aa0d71b97cb8a2e750ff6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62f88be226cc0142a60c66cc216cd65729e847cee7f9643efb5ff18bcc1dd45`  
		Last Modified: Sat, 16 Mar 2024 00:00:14 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eb529d23f61af8300756ff62410eca141d0db8ee81e502e281fdff4ed68df1`  
		Last Modified: Sat, 16 Mar 2024 00:00:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba46ca6ff379ccbbae3267ed349896ed7a6851f6c7c2f8574b6eaa22c4f17521`  
		Last Modified: Sat, 16 Mar 2024 00:00:17 GMT  
		Size: 87.8 MB (87835555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb33107b32680c3e09833a53cde889d41a8acf4b26cbba35e083bf1ed788c7e7`  
		Last Modified: Sat, 16 Mar 2024 00:00:14 GMT  
		Size: 9.0 KB (9020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c4b4b6697e86f3fc0cb8024dac0b5509482562402859e02526d2395a885226`  
		Last Modified: Sat, 16 Mar 2024 00:00:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880e70e76d044991eb65860ac410774db4973ff4b7fd7005db801885839f9559`  
		Last Modified: Sat, 16 Mar 2024 00:00:16 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25d3e40fc5037b14cfc1690b0f15bb477beacd32ab41c85eed367158ab820ee`  
		Last Modified: Sat, 16 Mar 2024 00:00:16 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca346356cad1ff96298f74e8e27e42f7d98b0ba84f70dbd5bab9cf1e869a62e`  
		Last Modified: Sat, 16 Mar 2024 00:00:17 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:87c830737b69fdd05d6025cf914f29fd109d337c2a8270104a97ab1cca4db05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.0 KB (990042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1b51545e87def83231853adf3708760a63210028087d52c4a45d4e1774ffe9`

```dockerfile
```

-	Layers:
	-	`sha256:7b71734c5098b424cada17d476e36705a217b68258481d77379a3812f01ee179`  
		Last Modified: Sat, 16 Mar 2024 00:00:14 GMT  
		Size: 953.4 KB (953410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:387d0b84315a1be500024d758d9889cdfc61524913083f895667f9c2b4af1d82`  
		Last Modified: Sat, 16 Mar 2024 00:00:14 GMT  
		Size: 36.6 KB (36632 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.18` - linux; arm variant v6

```console
$ docker pull postgres@sha256:ad830e4ef833be4ebc0cd45f574d11ac93eddc053cc55fdaa67453a5518ae024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89974058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d346817cfd688cce653a2fcdf2aacd50263205be437c9df0c54421686dc1ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
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
	-	`sha256:9065243667bb01d502ffd99d597da01fff35b49ce24234fdc0d8ac47609adcb0`  
		Last Modified: Mon, 12 Feb 2024 22:41:53 GMT  
		Size: 86.8 MB (86810690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f5b08ae159fc30a2d1ec701478ee3b92e966752afd114f012bfc823c8aec9`  
		Last Modified: Mon, 12 Feb 2024 22:41:50 GMT  
		Size: 9.0 KB (9023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b719f56cb946e6f7239eaa1a0ca09dfa2746b558acb8d49e9f39f4ce6390d6d`  
		Last Modified: Mon, 12 Feb 2024 22:41:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94d96a6790c8acd0576b44604ffb0f7dfa602592cdf3bd6de4e80c14f5fcbaa`  
		Last Modified: Mon, 12 Feb 2024 22:41:50 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4edbad9ab2a51b79527d2ca194daae6bcd81c87e82a9d018c86c42ded259f3f`  
		Last Modified: Mon, 12 Feb 2024 22:41:51 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e0282764f45132998ad47ff9f5be69e94596c519546712bcf51bcc3ddb788a`  
		Last Modified: Mon, 12 Feb 2024 22:41:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:fa73f59c1c6f42206d42b951d38231302bc78223f1b46bae87f00b7c1a31737b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e384dc995aa7f72173864d6f62dc8829892a575b7a617500fcd742ff654fccca`

```dockerfile
```

-	Layers:
	-	`sha256:3e4e79eb93ce210749b875fb7b5a01d870384afd440fe76e62360c031a3de7ff`  
		Last Modified: Mon, 12 Feb 2024 22:41:50 GMT  
		Size: 36.4 KB (36383 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.18` - linux; arm variant v7

```console
$ docker pull postgres@sha256:52e29ec678176893c993d69af99c911fb869bfce2672533b1498dddc8371c31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84674655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca8c746353328175ba405ead9a5007cc3df0bfdb0d20c2a03c19d18cd78a87f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
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
	-	`sha256:f4ea58441166e174067490c8d1eb6c716baef0902f6ae9c55ada7b3672f37228`  
		Last Modified: Tue, 13 Feb 2024 23:34:44 GMT  
		Size: 81.8 MB (81756957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cceedd835315f141e046fb1d6ab719b1bd37bf8f0fe056e732b7d29bc5adfcc7`  
		Last Modified: Tue, 13 Feb 2024 23:34:42 GMT  
		Size: 9.0 KB (9023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e53107347298265832968213c89a983a20bbf96c9a02172dcecc6b1f981f4a`  
		Last Modified: Tue, 13 Feb 2024 23:34:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bd06694f966cee7e889d6457bc269baadcc15fd6b53ba5f7a561172c24c007`  
		Last Modified: Tue, 13 Feb 2024 23:34:42 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383adf9e39de50456b258f8df0dc3b93003351cdbafbd64eb8ae60fc54cd5039`  
		Last Modified: Tue, 13 Feb 2024 23:34:43 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e54c66945f72876e5e2b17ba1939ec48b7ad695d5ab8e4409bb2460118da623`  
		Last Modified: Tue, 13 Feb 2024 23:34:43 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:798b0e751f22a23a443ef23bdd009a9401514da47614b18b1348c082ac943ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.2 KB (840250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a608f50367ab33d5aa2f245d4d6b6bf1112955bc36cc21f05a0d4289476bc822`

```dockerfile
```

-	Layers:
	-	`sha256:fcaafd6ee99c4436fff6ce0cdb4ac83b64a843e9e5bfe2053428cb3cfcce56ae`  
		Last Modified: Tue, 13 Feb 2024 23:34:42 GMT  
		Size: 803.7 KB (803652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d6af729145a0d5ea65edab66b9fce5b11b01e0ce075b102c961f93e5b8fb859`  
		Last Modified: Tue, 13 Feb 2024 23:34:42 GMT  
		Size: 36.6 KB (36598 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:45de1a6c1e06c8fb25391fc3ce324e21c6d96f1be5dfb0ccd16264c75e4117ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90241309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918243cc5062354c2e87acd14ce67199f7d8e885df9fcf2ac233192f76eb513a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
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
	-	`sha256:fc6c588e9bf0ef96409d57c47892db076444c5d408cc72b9a593c2d6e4348f59`  
		Last Modified: Tue, 13 Feb 2024 14:47:53 GMT  
		Size: 86.9 MB (86891649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36bf4506a63b2d1e5ae5dcda1c3f233b22b3650b97933a107af75b861952a94`  
		Last Modified: Tue, 13 Feb 2024 14:47:51 GMT  
		Size: 9.0 KB (9020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532012caa03ea0a9589c6ca4b7ff0492cba0e19be6cd5e7c584d4d992e2caa2c`  
		Last Modified: Tue, 13 Feb 2024 14:47:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7576ddba24730bdc4426dcd94186f469022378cb60ef00c37ffc9c9268dd25b1`  
		Last Modified: Tue, 13 Feb 2024 14:47:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5036d7dfc44438e88e6a159485955945c0beaee726f8b88ffcebe3fb43b7427`  
		Last Modified: Tue, 13 Feb 2024 14:47:52 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6481b8f60c7f8aeef7ddf45d354d5a88e7bf9aa192dbd8b5f810a290776d7779`  
		Last Modified: Tue, 13 Feb 2024 14:47:52 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:c0a2cd262dbe17510144533235e01a3666d26ade108380473a29c9b1d11d2cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.1 KB (840111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c59004ddb7b9ba599d1a77781b4cb2a55934f40de9538fd34c29d450537d028`

```dockerfile
```

-	Layers:
	-	`sha256:c63b1404a46371a3342dbe0b4641fbabbfb8cdd870cf4f87d6df51affc56e775`  
		Last Modified: Tue, 13 Feb 2024 14:47:51 GMT  
		Size: 803.6 KB (803639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c256ed4e41fd2355bed6048bdcbe5bf49e87c2d007f75045e2d09219bffbc7`  
		Last Modified: Tue, 13 Feb 2024 14:47:51 GMT  
		Size: 36.5 KB (36472 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.18` - linux; 386

```console
$ docker pull postgres@sha256:817c2b4cb60eb9b6df8a20078ce69adcd6056e4dc7298cb8bc4670405772aaaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96186732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83b0631c91c21a1d95762f705283e4ef5564508f381dc6b32280b5bbdb180c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
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
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9c24fc1b8958d365fb7c0996897ca9afd4ba8a76add42f2ba932242c07f8f7`  
		Last Modified: Sat, 16 Mar 2024 00:00:29 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67a9c4e20b18f5202e7c919e64e8a920c8c9f58f17e9ab9eda2c1dc9561f442`  
		Last Modified: Sat, 16 Mar 2024 00:00:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de071356f0b2cfefee4461c55816c9cc308bfa2ce7279da2756efeb56527f63e`  
		Last Modified: Sat, 16 Mar 2024 00:00:31 GMT  
		Size: 92.9 MB (92931362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c1d7a7f7e277cea6f0ad42f6a16098c7bbf3bba8586b778d97f6610aebe92e`  
		Last Modified: Sat, 16 Mar 2024 00:00:29 GMT  
		Size: 9.0 KB (9022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67eb691b206cce611d1ace22d962f893128d2bc92a17b69a91ac0cddf9f7ecfa`  
		Last Modified: Sat, 16 Mar 2024 00:00:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77e2c6aa6c6fac486f472f8f4d136ad55d506055a495bd035649685979fdeac`  
		Last Modified: Sat, 16 Mar 2024 00:00:30 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a595bba1a719fd8b35420566ea440e658106e36d1b83b45002e56c16e81b80b`  
		Last Modified: Sat, 16 Mar 2024 00:00:30 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cbe63512a2ad0ddc3596f9371b53b5b4824287b393a95b1451e70640a06cb7`  
		Last Modified: Sat, 16 Mar 2024 00:00:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:2cd4a6497a4564506e86b0afbc60a7f4eab0e2ec2fdcf1aefe98f1de63a93c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.0 KB (989996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d7f11f348c7020401f883451103a5c6a56defa589211736fd76719f1839be6`

```dockerfile
```

-	Layers:
	-	`sha256:2f6ce35fe6116edc38a510f1dc55d0ef410525aff7db1afa936700a189fc428d`  
		Last Modified: Sat, 16 Mar 2024 00:00:29 GMT  
		Size: 953.4 KB (953395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d414ed5844737317ee5e4788e4d39353fe893670dbd643269a6dab5c7b8913f1`  
		Last Modified: Sat, 16 Mar 2024 00:00:29 GMT  
		Size: 36.6 KB (36601 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.18` - linux; ppc64le

```console
$ docker pull postgres@sha256:40c55e142f08da84428026c93499dd49cdd6059ed0416636ddec70384c912e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96780352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f3a42fa4d93c93f85ac890ef00ff3fe39004d9abd03f10afb44a0998f92a04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
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
	-	`sha256:2e913254d91fe8081d30f572daa3e2b5a2fbffb91a077d281f503afba7646fd7`  
		Last Modified: Tue, 13 Feb 2024 00:20:23 GMT  
		Size: 93.4 MB (93415562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247123c81da175b3311184f7168dc2ce29b3fde35453ec98790205f998d92380`  
		Last Modified: Tue, 13 Feb 2024 00:20:20 GMT  
		Size: 9.0 KB (9021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1faf91fdc44a2f13c2f4d535ad8fe060e9ad57dd3da07138556c9c65a1ea04`  
		Last Modified: Tue, 13 Feb 2024 00:20:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87914e450b82fa32e5586e0b3fa11ef61c47516bca164cee0cb90f6df52aa360`  
		Last Modified: Tue, 13 Feb 2024 00:20:20 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d24dcdc01d57ee8e59bf5454968bc3bc13fa0df7861d4aa62ddf32d0c34b1c5`  
		Last Modified: Tue, 13 Feb 2024 00:20:21 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8086caf648aec220723de9a58f504b1b093babdae3225c8fe70dfde8f7b85664`  
		Last Modified: Tue, 13 Feb 2024 00:20:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:55568c5e837d887c8e5327e29e194f6424657fcc746fa7f18d4b99e7c3540f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.1 KB (837107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c035693457d1d217c6c5bb36aeaba35d9222fee10285f2f0e9bd5ef67cdda3`

```dockerfile
```

-	Layers:
	-	`sha256:cbb101a9c9df6ae6a0d99def79c460285a50c97ebdcfd54dc1def58b39230e9f`  
		Last Modified: Tue, 13 Feb 2024 00:20:20 GMT  
		Size: 800.6 KB (800603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f748f6ee9c52368e212235575c1dbd1cec4e079d87de1e84f8e9b75a9a3e08d`  
		Last Modified: Tue, 13 Feb 2024 00:20:20 GMT  
		Size: 36.5 KB (36504 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.18` - linux; s390x

```console
$ docker pull postgres@sha256:af02ce2ebb70490f1875bb672f7de95ff8a957a227e47cdf77dcbf9823e8788e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92864387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45dd8106901c537cb3550bac2631be9839a43c236471c46f9e1df253a12c0ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
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
	-	`sha256:c30716ce5e06f4e5452b54185fa863bdb64b5bebe8526a9b3199ee69794381da`  
		Last Modified: Tue, 13 Feb 2024 23:25:00 GMT  
		Size: 89.6 MB (89630552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a228f0699669b1c739bff3061b36f58a0d1411095e120a44df738d9fa363a4d4`  
		Last Modified: Tue, 13 Feb 2024 23:24:59 GMT  
		Size: 9.0 KB (9023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89d9d8d1512098a4e30d357efa31bf7c37900cdd866b5223fc0f3d59ca72385`  
		Last Modified: Tue, 13 Feb 2024 23:24:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461dd35870f85a3ea84988cdd67887733899d6df2bc03ed50a4c3ff7d8014914`  
		Last Modified: Tue, 13 Feb 2024 23:24:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d60ac7c27929a84e6fced97b45f1d9691881307cbf82baef430f419fcab69`  
		Last Modified: Tue, 13 Feb 2024 23:25:00 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78929818c7f2b1bd1c7f33c9a774ed91fbe81aa4bf641fb06b88dab5c640578`  
		Last Modified: Tue, 13 Feb 2024 23:25:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:908e6ed07cfeb6a21acc0364cac6679cc812e71293471d9e34973b52c0f4ee49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.5 KB (838462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c538cb02580659d818b692a9ff869577a56ff58041bb2be1ccc77617b0e2c8`

```dockerfile
```

-	Layers:
	-	`sha256:bd889f3079bd79fe73ccd1d7898b8c73e9ba0a40adda5d5b1e5b9cd55fa8dc7e`  
		Last Modified: Tue, 13 Feb 2024 23:24:59 GMT  
		Size: 802.0 KB (801996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174f2f285bbaa11f9ff819f33494c2252e14179ebbcb1f0c9f01628d32835b9c`  
		Last Modified: Tue, 13 Feb 2024 23:24:59 GMT  
		Size: 36.5 KB (36466 bytes)  
		MIME: application/vnd.in-toto+json
