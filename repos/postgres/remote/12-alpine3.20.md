## `postgres:12-alpine3.20`

```console
$ docker pull postgres@sha256:f98c0d178063858e37e0ecb3ee493d87c2347732313c41cdd60a46943c66c711
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `postgres:12-alpine3.20` - linux; amd64

```console
$ docker pull postgres@sha256:d6b72c2bad867fe00a05e8bb9582d30c482580755a345618b6ad91ae78c952a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92015969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9cf14bff81f13565f2c8d98255baaa7417ad7186d8d254120c2baf623cff840`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV LANG=en_US.utf8
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_MAJOR=12
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=12.19
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=617e3de52c22e822f4f57d01d5b2240503e198a9eccaf598a851109bd18e6fbb
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 22 May 2024 20:39:44 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 May 2024 20:39:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 20:39:44 GMT
STOPSIGNAL SIGINT
# Wed, 22 May 2024 20:39:44 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 May 2024 20:39:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8734184271f56f32cdc48b584513496f76d9c687ca5cb94f49a6f07052610d8`  
		Last Modified: Wed, 22 May 2024 23:59:12 GMT  
		Size: 981.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11fe8e4281ae6b30f46cd3937663148ede7a46e3f98ac3a64cfa8b600ba78d7`  
		Last Modified: Wed, 22 May 2024 23:59:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ac0fd28b4d2220b80efe6b07aeb8824424be21f0c7393cb9aa64da478f3d64`  
		Last Modified: Wed, 22 May 2024 23:59:13 GMT  
		Size: 88.4 MB (88378187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537496f980d40cf617603703f5b16c8422dcdef1197d12a2d2137434766b8fb0`  
		Last Modified: Wed, 22 May 2024 23:59:12 GMT  
		Size: 8.7 KB (8686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade7dd2c1b2687098f24f58e2190de25c19b93e7fc013af88cce9fe190128795`  
		Last Modified: Wed, 22 May 2024 23:59:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c3745855d5785b9d135a20b17d900d488af2a80c273b57a2fa2cbbb1b3703f`  
		Last Modified: Wed, 22 May 2024 23:59:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593f9efa82acb5f0954b045db223dd82a0d8a60aca5ae9655191b6b29bcc920d`  
		Last Modified: Wed, 22 May 2024 23:59:13 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c440293c36b74eb6dcd81b13715ba28ccc1937081b5d3ae1242d36e464c1f45`  
		Last Modified: Wed, 22 May 2024 23:59:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:bec4d6e9b9481990b98839996ceaecd1ee6289eb776ef78c903337fe614a04c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.6 KB (613605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1b6c60cdd776884e072f081c12291b517d8a0e0ad424493403979b0bbfe41c`

```dockerfile
```

-	Layers:
	-	`sha256:4f7db90dca7e77037face7529c2c5380d4d93f1c36596bca5c7b7864a9f90637`  
		Last Modified: Wed, 22 May 2024 23:59:13 GMT  
		Size: 576.4 KB (576355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f38212d191a67c2bc72aaf65b8c56701a38e68063f4ed7e7c8b5d4926c8a99b7`  
		Last Modified: Wed, 22 May 2024 23:59:13 GMT  
		Size: 37.2 KB (37250 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:3162dcc1c698f16009525be5cbcd125a964fa8e027f929bf96b1751af6c5f504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90932145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7712207c7eeef8ed88bd149280a4e7dda4984097f2bf1163258089163773083d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV LANG=en_US.utf8
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_MAJOR=12
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=12.19
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=617e3de52c22e822f4f57d01d5b2240503e198a9eccaf598a851109bd18e6fbb
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 22 May 2024 20:39:44 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 May 2024 20:39:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 20:39:44 GMT
STOPSIGNAL SIGINT
# Wed, 22 May 2024 20:39:44 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 May 2024 20:39:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488c12f7241f8fc1619496d0d9d0cd195e25eff576860b2c2fc6ca7b1b2cd31a`  
		Last Modified: Thu, 23 May 2024 00:04:16 GMT  
		Size: 978.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c861b766de241bc0614704b27253da7792cf04d055bdac6cddc8c05b2f7b2f0`  
		Last Modified: Thu, 23 May 2024 00:04:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480b52b710b92f651bfe264843c70812fcd1e54b793e951f300babc7e19c1581`  
		Last Modified: Thu, 23 May 2024 00:17:12 GMT  
		Size: 87.6 MB (87551409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104cc904b6098cbdde65f0546873aacfad6ed31a97855be4813961463bcf4208`  
		Last Modified: Thu, 23 May 2024 00:17:09 GMT  
		Size: 8.7 KB (8687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90b3352e96296d405c439454d8b20dc8b285f3e51a7f133b19eab4201a3d77e`  
		Last Modified: Thu, 23 May 2024 00:17:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb5cac9f49f24983ea05ad699d995191605f8cc8bb5f4259c02633d8fda347e`  
		Last Modified: Thu, 23 May 2024 00:17:09 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ddb4c701933719b5d68a28b5c6d0718c59252e39354aa9942e0bf23c17ec3a`  
		Last Modified: Thu, 23 May 2024 00:17:10 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ca7420aa5b3280666a0befcbbfdb8322ab072875bbb6b9a64298f1b4ea480f`  
		Last Modified: Thu, 23 May 2024 00:17:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:50a3c3b1c8fed7204751fc0f16121a84a439d1b7d3816c9ec9557f2592eb1f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 KB (37013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8ea9799d43299d871385d2af9cbc1faee8ad24ba135a5e84de0e52c6eeed92`

```dockerfile
```

-	Layers:
	-	`sha256:867fc5a841dc465eb9423f6883434df1e64b331890035d23cd8dde5405200959`  
		Last Modified: Thu, 23 May 2024 00:17:09 GMT  
		Size: 37.0 KB (37013 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:69dc6468f7928e9a66f55fd25eb4e7536c2cc40690f5c8f224924d3c60f0b8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85443607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c67bb01fe5b61e160e13908aec0787445e1c13a893156def1d5a5c6545e095`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV LANG=en_US.utf8
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_MAJOR=12
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=12.19
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=617e3de52c22e822f4f57d01d5b2240503e198a9eccaf598a851109bd18e6fbb
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 22 May 2024 20:39:44 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 May 2024 20:39:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 20:39:44 GMT
STOPSIGNAL SIGINT
# Wed, 22 May 2024 20:39:44 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 May 2024 20:39:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfcf42c43f866e18aaea8ebded327323f09b2078fcf795fdabccf5beba409ae`  
		Last Modified: Thu, 23 May 2024 00:47:46 GMT  
		Size: 978.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024165db62c15a8a795ac5b1220a322ad3720e5297b7e12d65df63ceb28b747f`  
		Last Modified: Thu, 23 May 2024 00:47:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25317ad1a40623089b3242980befee278c5a5ee396c64cf72b1bfc63370a2997`  
		Last Modified: Thu, 23 May 2024 01:15:34 GMT  
		Size: 82.3 MB (82333894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0ce954b0e6f4d147ff2fc7b15238a9eb6225d0f396f812ca68080130826f26`  
		Last Modified: Thu, 23 May 2024 01:15:32 GMT  
		Size: 8.7 KB (8685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aef6d1d67b5a9349578fee3afa7a27716e3296e55f6491306bbacf3e995f3a`  
		Last Modified: Thu, 23 May 2024 01:15:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2801cad2fde1084debfcfca3b7409ece755986e402564c399c02d289800b28`  
		Last Modified: Thu, 23 May 2024 01:15:32 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560c04cee3161fb8e1a2c4a2d6912619223cc0b8fbda1f97e86808e4328d9b94`  
		Last Modified: Thu, 23 May 2024 01:15:33 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85067a3840251c648d19b1572ea1e360ed58182e39782eba923e107170a99c2f`  
		Last Modified: Thu, 23 May 2024 01:15:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:283279b9dd84e9a9603b41d9a1ff4582406ced99629768e6ba64e74abeb6c065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.6 KB (613622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a5538b9637974caac24910a6d148850e7bcdad6bf945d50447d8b8f4a61f06`

```dockerfile
```

-	Layers:
	-	`sha256:822439ef719f0a9019fe4e14ffe09ff46ede3840bed417c1df3a2fb1340073eb`  
		Last Modified: Thu, 23 May 2024 01:15:32 GMT  
		Size: 576.4 KB (576391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:974c36cb557978888fae0c1970460066e4d8e837887297961f99b3b4520dda2a`  
		Last Modified: Thu, 23 May 2024 01:15:32 GMT  
		Size: 37.2 KB (37231 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:d6ce4ffe84864a8f976989fa1c81f874ca5bbaa749e27153aacd6de6d3733425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97285392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8444872431799bf8fce1d334a9d7a1e7a19ff9bb9beeb0b41cb70fd35c7d65`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV LANG=en_US.utf8
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_MAJOR=12
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=12.19
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=617e3de52c22e822f4f57d01d5b2240503e198a9eccaf598a851109bd18e6fbb
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 22 May 2024 20:39:44 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 May 2024 20:39:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 20:39:44 GMT
STOPSIGNAL SIGINT
# Wed, 22 May 2024 20:39:44 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 May 2024 20:39:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99524fc2fb9625731eea937ad6f4995ea06fa8dce28900de9e797aaa714895b`  
		Last Modified: Wed, 22 May 2024 23:59:22 GMT  
		Size: 979.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d171c8d2d8b1300e797376550992a11518f68090d8847031a105c938ef916a`  
		Last Modified: Wed, 22 May 2024 23:59:22 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa78cd4313bcf52b80fc038ac5812aba9f6d095b131e7f8167d026b38b23f6ea`  
		Last Modified: Wed, 22 May 2024 23:59:25 GMT  
		Size: 93.8 MB (93802531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844709abfce5ef9a4a5bfe803a267953095877d9ff9529d2877aa17a9df42fd6`  
		Last Modified: Wed, 22 May 2024 23:59:22 GMT  
		Size: 8.7 KB (8684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54a934907079b1ae5c15551f5506be748a7661f6f2fdf6a1bdc0f34da8264f9`  
		Last Modified: Wed, 22 May 2024 23:59:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774bf78c54e7cc27df699fefa3a61f880956aa0456e49364c6f4dc9207adc551`  
		Last Modified: Wed, 22 May 2024 23:59:23 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05eb0a13b9b3a4c8aa794b43e1233cd2b0e9993c2791f98e9c95103055be90a`  
		Last Modified: Wed, 22 May 2024 23:59:23 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fd3ac75f771f0a30cd9e9ec87c276408e655bafc9b849459a34b12bdcf7a6a`  
		Last Modified: Wed, 22 May 2024 23:59:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:284815f24bfe9ef900e857ff952da85e4d3cddd78b5a1c6cd6c57c04d135c1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.5 KB (613539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c5452bcd308f72d9211310117f005a9f79f981e6fd7bacd8ccb249e9e9aaa9`

```dockerfile
```

-	Layers:
	-	`sha256:fdbcdacf707e69ba787efa5eacf926a2ab3f105f2aa6fccb64b5bf4d4a54829f`  
		Last Modified: Wed, 22 May 2024 23:59:22 GMT  
		Size: 576.3 KB (576330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a389399917773bcfc176ea86875331f1317166336ddf860cbb7ff470c6f025c3`  
		Last Modified: Wed, 22 May 2024 23:59:22 GMT  
		Size: 37.2 KB (37209 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:156cde3fe46f26e61e883528d9b11fd58c4fe0b51373004ef0c8ee89e432fc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96488178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9c8624478363ccf25325348d3cea4242d8b16decf2a6e3a1fc1826a8ecb781`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV LANG=en_US.utf8
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_MAJOR=12
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=12.19
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=617e3de52c22e822f4f57d01d5b2240503e198a9eccaf598a851109bd18e6fbb
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 May 2024 20:39:44 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 22 May 2024 20:39:44 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 May 2024 20:39:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 20:39:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 May 2024 20:39:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 20:39:44 GMT
STOPSIGNAL SIGINT
# Wed, 22 May 2024 20:39:44 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 May 2024 20:39:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3b02b639f60b95c8bee42965fc2865ea862fb498bba9bb97d5948c11d6e061`  
		Last Modified: Thu, 23 May 2024 00:41:48 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc56b9f64c4f38953ead8536055652cb2059e7ade17f1f4541ab8b371fae904e`  
		Last Modified: Thu, 23 May 2024 00:41:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7788893e6373c4a35beb99ffe8d86f12e24cbe55eb15c81d9c1dbe2e42c863d`  
		Last Modified: Thu, 23 May 2024 01:09:32 GMT  
		Size: 92.9 MB (92902649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5712d89b8b1220a7d36f0d645919afc4ce6addd60f2d700da6c32393edb5fe`  
		Last Modified: Thu, 23 May 2024 01:09:29 GMT  
		Size: 8.7 KB (8688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d7c9d7bb4819d337b5db12ce9bec14a3df5b38cacb84da5e3e93839ad7c1fe`  
		Last Modified: Thu, 23 May 2024 01:09:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed3a2eaa39f7972742c2da7bdcfa870318fe59b6789444265489abd021c9eda`  
		Last Modified: Thu, 23 May 2024 01:09:29 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2625ab7ed3fd0c1ff8594c4dd959b300e1aee90f56a1b97d9b7f2528bd1148`  
		Last Modified: Thu, 23 May 2024 01:09:30 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0998aa6c79c915fb0453616470346016c26ceaca1faaa795ab50ad36895cf519`  
		Last Modified: Thu, 23 May 2024 01:09:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:89685cbd37417121e2662a7242299030c765b1e3b64761a1db02fc27adddb141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.0 KB (610048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1215fd20fb3511d1abc1592b850913db1bbbfbf09f396c3ea693f30fc1ec06`

```dockerfile
```

-	Layers:
	-	`sha256:fb2b33dabe95c53175341bbc3c6b8903f81fd2c64a543fe6916567839428d99a`  
		Last Modified: Thu, 23 May 2024 01:09:29 GMT  
		Size: 572.9 KB (572914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f2849793385a4368ca1051dc0cc154a48374b5ceca040fe5c9f454664f88f14`  
		Last Modified: Thu, 23 May 2024 01:09:29 GMT  
		Size: 37.1 KB (37134 bytes)  
		MIME: application/vnd.in-toto+json
