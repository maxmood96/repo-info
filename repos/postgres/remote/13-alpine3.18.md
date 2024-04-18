## `postgres:13-alpine3.18`

```console
$ docker pull postgres@sha256:9e440d938cd81cdf38fe104d79c6e1e2f7277cd39577e2e90d42c9793134ede5
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
$ docker pull postgres@sha256:90a55445bf4fa47fd511b772606ef919478daf73f1146ed8ae555ac65eff5876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89974113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31344792cd52de95e5254797d78ea428c9d8c74015f03ba49ebf85dc6773277`
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
	-	`sha256:ec3e7cdf7bf86da245d1f7f52ae282da6244162a7f75f85c1db59817457b132d`  
		Last Modified: Mon, 18 Mar 2024 16:12:02 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818a5c42b0910ffd2d1baa7ddcdf1397decf725a96001d7c8e4400432a0c8398`  
		Last Modified: Mon, 18 Mar 2024 16:12:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b25a41d56ce045afa85f082fbf9d728933c71a6fe6e7f00c8cce5718557454c`  
		Last Modified: Mon, 18 Mar 2024 19:37:07 GMT  
		Size: 86.8 MB (86810749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1bf6f7c1f2aa8fb5e36bc26fa2d98177c196568029b770e39f3a0ef608dd01`  
		Last Modified: Mon, 18 Mar 2024 19:37:04 GMT  
		Size: 9.0 KB (9021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1458756a214c0ba0c9fce2dd3a7b47f623b2465d42b0a397aaf8bece4e14382f`  
		Last Modified: Mon, 18 Mar 2024 19:37:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41005483d9bbb087620f8d690bf87ab3c89f538846b5f530b692c1d8e44589f`  
		Last Modified: Mon, 18 Mar 2024 19:37:04 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0569457e0857add4c02563e9ba8541d1eae7417601161ab7cb0409c6a65329`  
		Last Modified: Mon, 18 Mar 2024 19:37:05 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6783b882ac79048b6b6370fdea42647fe8aa70d152672c66487cc48fcb8cb997`  
		Last Modified: Mon, 18 Mar 2024 19:37:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:bcec0b2d07b7b24cc4c1ba440b811603a207ec945ec6d382f0956527dc3578dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b02e834f8c21706b28d3ac0b927bbf3db9eac72fbbf1a25f2fdae1636a62be8`

```dockerfile
```

-	Layers:
	-	`sha256:3322f6152ad816a97d9da662357896309a1a411b4999d3b5df49fb28d0354069`  
		Last Modified: Mon, 18 Mar 2024 19:37:04 GMT  
		Size: 36.4 KB (36383 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.18` - linux; arm variant v7

```console
$ docker pull postgres@sha256:f62b37f8bae762f285f97bd0f9082f5bdf595fd6679d6ce6d9a7fb2b8e3d92fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84674585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8513c228e80c71a0106d9520e57bf19946f5857edcbc3674e9d294d727040dda`
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
	-	`sha256:dfd951a98e9bc26ad55202a730fbf176a99a4f1dafeac246adac9b93116e6841`  
		Last Modified: Sat, 16 Mar 2024 16:26:55 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83b4bffee9860001c77fb26ccc9519a32dcc2324e1b6490008d4eee80c0ab7a`  
		Last Modified: Sat, 16 Mar 2024 16:26:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f0385d524d4ac8d6b35611942521807cb8e83811fb40f78e0fdfa92809ad48`  
		Last Modified: Sat, 16 Mar 2024 16:58:57 GMT  
		Size: 81.8 MB (81756890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77230357f99e774ee288425bfce559e2752f2289a4d58d1b24906063acf69642`  
		Last Modified: Sat, 16 Mar 2024 16:58:54 GMT  
		Size: 9.0 KB (9024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a340032531243027c0bc6c71d0978532d1c8d8867de18a8d475d95f6dfd92653`  
		Last Modified: Sat, 16 Mar 2024 16:58:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fef0cc2d25211574aa5712eb42bf0e314440ed015bdafa249a96739888f312f`  
		Last Modified: Sat, 16 Mar 2024 16:58:55 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6356f78149a47f9ca5bbc3a5f6c86dd82a520f942c4eefec13fb83d37b406fd9`  
		Last Modified: Sat, 16 Mar 2024 16:58:55 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da50d63f1365635ce36bba1cd554dd4ee943f197848eab0fba220f410c5f2178`  
		Last Modified: Sat, 16 Mar 2024 16:58:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:40c4044ab09d43088f39afd88d8f3ef14860581d4cf93661806b3f3847dc835c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.0 KB (990028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066df27d33878f6bcd12296c6c40fac609b4db5d309d6dd6eb1d6bae492e696c`

```dockerfile
```

-	Layers:
	-	`sha256:f4441bc751d3b8472bfdaf20864fd157ce91c36c970f1307480a180d89328181`  
		Last Modified: Sat, 16 Mar 2024 16:58:55 GMT  
		Size: 953.4 KB (953430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39d0611c811a7f66097cfe08da386919c2592bd47921f37cbf9515f0fb6c33bb`  
		Last Modified: Sat, 16 Mar 2024 16:58:54 GMT  
		Size: 36.6 KB (36598 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:14cdf53ac5c807aa4448b72b2fc26108b09e68cc76cb4c4776dbcc7666dd4b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90241281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be24c7cabe5d8b02889092ef0443046f412ae6d0f310c7e854a6aa97165db34`
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
	-	`sha256:9f0d67f8ee92283d3a70b55534935f9cf573a96846e14b450142f2ee97b0abd7`  
		Last Modified: Sat, 16 Mar 2024 16:13:31 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c4fb2be86da82b8c1a950f073ffb3f9c21075f9798fff81fd347e8cfa19b84`  
		Last Modified: Sat, 16 Mar 2024 16:13:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6b958f2e116d3448cbf454aecf1d9cfed909030847de1bf283934d89f03625`  
		Last Modified: Sat, 16 Mar 2024 16:29:35 GMT  
		Size: 86.9 MB (86891616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968955c23a75d00614a1c5fa0534e5e18bbdd8a660d195f0945c6222bf353342`  
		Last Modified: Sat, 16 Mar 2024 16:29:33 GMT  
		Size: 9.0 KB (9023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c8ca43cf56519b14bae72b35ab1a11da32428f896ccf3e7ec2d41e9fbc1216`  
		Last Modified: Sat, 16 Mar 2024 16:29:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe78b1d07034d4c07df6054a5e794467e54e89ef2a0c27862497100c67270221`  
		Last Modified: Sat, 16 Mar 2024 16:29:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1719122da14f3982087ba8b46c05de98ee94750000c23aafa667ca9d2c4e31c9`  
		Last Modified: Sat, 16 Mar 2024 16:29:34 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dabdbe14c64b4a79e209697e3dee57ab2c7aaf07de4285b047da2ed2597cf73`  
		Last Modified: Sat, 16 Mar 2024 16:29:34 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:63179f1a3f796fcb1880b79f0324f9d6d6f2d0752e3db4645d0b0a2975c5f02b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **989.9 KB (989889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796be7977313ae88104e4967d3c49784d52a048e3e83176f9217522a6a536fb9`

```dockerfile
```

-	Layers:
	-	`sha256:314f83c44c8cd603a2306c1e8e5bee7c60f0070cb55e8541be920f540096e729`  
		Last Modified: Sat, 16 Mar 2024 16:29:33 GMT  
		Size: 953.4 KB (953417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:704c5982daf28b34e4bbc369540991d4c311df4e617c6b3d30e02a235082fd9a`  
		Last Modified: Sat, 16 Mar 2024 16:29:33 GMT  
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
$ docker pull postgres@sha256:b7e913a2b99807283dfaf385a0f3db7ab5e63ff55350c0431a2453b5e8a30466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96780117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2781858e338cab1e85cff3ab59487f95777af9943b44ab25905ad78a61eee80d`
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
	-	`sha256:57bf06424f58ac7307d52d4ae986fc96c03d14c3e8c9546673273e53c183a35a`  
		Last Modified: Sat, 16 Mar 2024 10:40:30 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545ceadfd5057505b4e5d6cd51ddf57b0cb73f291f5b2ab2e392c78a73f6318c`  
		Last Modified: Sat, 16 Mar 2024 10:40:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51eb5fd323b381940bb7687c2e21a53fb037dc47694c853b34e7c4e0c7dbdeb`  
		Last Modified: Sat, 16 Mar 2024 11:11:15 GMT  
		Size: 93.4 MB (93415322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38f574dee149378c0b15ceb9ed34af604430c8688380a5a05542aa57f2d1986`  
		Last Modified: Sat, 16 Mar 2024 11:11:12 GMT  
		Size: 9.0 KB (9027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b091fee983459283bc33232508fb2ca284d172306222d885de30eebc1480bb`  
		Last Modified: Sat, 16 Mar 2024 11:11:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4e6f2c181cf17e6f96ac9e45429a8c4f067359f600d8c0f66416775df2c3e3`  
		Last Modified: Sat, 16 Mar 2024 11:11:12 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f20e15f04d107891b0677ac2e4cb67899bd49c21afc9cc1a8c240f4f612eabb`  
		Last Modified: Sat, 16 Mar 2024 11:11:13 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74309de67c57cf5d26a43eeb2c2451db1213a9311b3762ad0a2e66033f3627d`  
		Last Modified: Sat, 16 Mar 2024 11:11:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:33e0722045bb78cdfacfcc4f5bf42d7e97c2678b85bc1f31ae4d502f71983707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.5 KB (986461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9e651ab5ee7a97388a9feae83edfa77bc26e6e4e6ce6992d0ee37748313d94`

```dockerfile
```

-	Layers:
	-	`sha256:c3b9bdfa9747c7ddef4ab6310b0a0dd8f62a065473de7f6bf272e0280813dd8f`  
		Last Modified: Sat, 16 Mar 2024 11:11:12 GMT  
		Size: 950.0 KB (949957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb985cb2cca159f303b6a8cb479695752f8175b01e278491420e448e5965139c`  
		Last Modified: Sat, 16 Mar 2024 11:11:11 GMT  
		Size: 36.5 KB (36504 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.18` - linux; s390x

```console
$ docker pull postgres@sha256:5c1b8d301bda954a54c654ffefcb2de41ea7b0ce0d55ead70afef505708b83ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92864515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659c730b5b21ee426911d414ecbdfea29953a71ef418208e28bd04f0f1c074aa`
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
	-	`sha256:cf260decda6a63ec1e1aad448e571ec50e25aa04f4fe41a8a7c8467fd1d98040`  
		Last Modified: Sat, 16 Mar 2024 10:25:45 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072023fa977b97bad79fe5490620d4365467a2f39216fbc49cdba3aeaffd97b8`  
		Last Modified: Sat, 16 Mar 2024 10:25:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38e7efee8b7c7f62d72b6b0d93638dd9790b77f39300641c1c56fea8cdfa2a3`  
		Last Modified: Sat, 16 Mar 2024 23:17:24 GMT  
		Size: 89.6 MB (89630676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3984bcda427324bceb23f1d49f123f0f001b334c2f2421169cde757e6412b1c1`  
		Last Modified: Sat, 16 Mar 2024 23:17:22 GMT  
		Size: 9.0 KB (9025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8e6bc2a3d13481a994a83dab6d3fa7b95ae3d1932c324ace027219f1e15f66`  
		Last Modified: Sat, 16 Mar 2024 23:17:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45ce992b916af705da117ab7ccd591e9b4562f0a87dd25a6d1d16a5928e552d`  
		Last Modified: Sat, 16 Mar 2024 23:17:22 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5822edaefc22610d133f0ed9064a7de818f3d2810c69d5a6d8f6301057278374`  
		Last Modified: Sat, 16 Mar 2024 23:17:23 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465eeeb42cfbd6ee47f60c6e4746be985577fec8782b0ff2516c1f74d19c08df`  
		Last Modified: Sat, 16 Mar 2024 23:17:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:69578ede28044f3a6f9a795e6b8a582b404693a454a61fa84686858e70a6387b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.9 KB (987921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a583049c52202889422c3cd29a9858f2b1a3739cdd062c869e2e1843335ebc50`

```dockerfile
```

-	Layers:
	-	`sha256:02d3b00c07c80fb6319bac1518d6efe0660ab69692e36d9d6f902d19c36cc967`  
		Last Modified: Sat, 16 Mar 2024 23:17:22 GMT  
		Size: 951.5 KB (951456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ad1add1ea0803fda268b5927340d8881a75281ae850483b2c4828ff58816503`  
		Last Modified: Sat, 16 Mar 2024 23:17:22 GMT  
		Size: 36.5 KB (36465 bytes)  
		MIME: application/vnd.in-toto+json
