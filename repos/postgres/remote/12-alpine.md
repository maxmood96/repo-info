## `postgres:12-alpine`

```console
$ docker pull postgres@sha256:f1cd4c31e0eef9c6a7feae86679266199435e63c1906992afb9bf8a693e21a57
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

### `postgres:12-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:aabc37fc16dc65009ebebfc0e4cfa8a526e8de16ac22144e113066be07d3d22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (92015439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207afba18c6ce12930ee5c598c4ce1db6171d03c51223134f59d56355e94913d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=12
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=12.19
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=617e3de52c22e822f4f57d01d5b2240503e198a9eccaf598a851109bd18e6fbb
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c461540c87a1a862384b2872d63dfa9b1dd9f600ffd077356fa8c5360c5e3444`  
		Last Modified: Mon, 03 Jun 2024 19:04:54 GMT  
		Size: 981.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0372a911ffe82ad07f4880bd25192e214d3dff487932c4f0f846a5ac3f8ea06b`  
		Last Modified: Mon, 03 Jun 2024 19:04:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc29bcee5c281903fe7461786e8b8508db9aacdc06d5f3609efecd764910e58`  
		Last Modified: Mon, 03 Jun 2024 19:04:56 GMT  
		Size: 88.4 MB (88377662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea168d6786dbb7a413321de1e0f43b32e75ad27594e1c3621b0f7e1adcdd6f86`  
		Last Modified: Mon, 03 Jun 2024 19:04:54 GMT  
		Size: 8.7 KB (8684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a61dad673e0f2016acf0e5cff566cdd2ac915568aaa355c0747e66b2a64c1e`  
		Last Modified: Mon, 03 Jun 2024 19:04:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ae7c67daae4b43c8d717074e1d4a800a774bebae819dd0b7a5aeefa722ce34`  
		Last Modified: Mon, 03 Jun 2024 19:04:55 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f23392cffbec088a2c78228bfdb1f9b94a343c639621f3d55f5e87146c57bf`  
		Last Modified: Mon, 03 Jun 2024 19:04:55 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a6e7427563fcc428710890520611ea728f344a3a9aa51ffdf4e36b5b7fc28c`  
		Last Modified: Mon, 03 Jun 2024 19:04:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:64d324028c338178644b348585016aae20150a0c6f54813ae9c58321246f7255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.5 KB (613454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b47ade5f863bca79b0b8994e50b15507b725c2c059e905e3e2074e0fa217eb1`

```dockerfile
```

-	Layers:
	-	`sha256:956e37e5cba60043891e5832e7e7c3ea57abea11c5cb5e0039bdeff0bf7e9ceb`  
		Last Modified: Mon, 03 Jun 2024 19:04:54 GMT  
		Size: 576.4 KB (576354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:babb20c81f23b71addb1d9b54682d27f7c19c0f01a2498c5a7bb0b534e39436c`  
		Last Modified: Mon, 03 Jun 2024 19:04:54 GMT  
		Size: 37.1 KB (37100 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:102ffb9c4e5490ec72f3382bed716eaed2e1b9ae52337fd4800e8089a0364893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90931708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5d9b18c561b08a6b9e2d06d260e0bd1ee748c27fd64edccfde161bb533ab60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=12
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=12.19
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=617e3de52c22e822f4f57d01d5b2240503e198a9eccaf598a851109bd18e6fbb
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c63537711e2b71098dfef581dede9863d3952e51cf921a6044c1ca139319887`  
		Last Modified: Mon, 03 Jun 2024 19:21:48 GMT  
		Size: 979.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687782b67bec9f1ff4f194d23363629e4e78d8095a9aacd4311a20f5b9473ff3`  
		Last Modified: Mon, 03 Jun 2024 19:21:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44853a39e0af3d38d323193b83751d4632465e8f5155d5d0f0936710c86df1b`  
		Last Modified: Mon, 03 Jun 2024 20:06:53 GMT  
		Size: 87.6 MB (87550968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176f5de948b50ba32f726c02791f49feacfb1a0e5e6274a352960aea802a0f26`  
		Last Modified: Mon, 03 Jun 2024 20:06:51 GMT  
		Size: 8.7 KB (8688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c9d2b9088bbc1cc05caee3324713c2c2e01d2bb7338dc0d49523ef98ae3f27`  
		Last Modified: Mon, 03 Jun 2024 20:06:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae7650643c8c075d5a28e11917f00953ee091d0a6f5a411cd20c77db12b7f79`  
		Last Modified: Mon, 03 Jun 2024 20:06:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c45f0a1c7e4f137222ce495c8859c9c1a6821f879e5b42a13a5497e309d0709`  
		Last Modified: Mon, 03 Jun 2024 20:06:52 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1670d9c89942989e6ec5627c1deae838b15be55f093c9a8600d4aa79b71f5a19`  
		Last Modified: Mon, 03 Jun 2024 20:06:52 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:a4bd8436b12df7084f2d1e70523663b96c18c686dd45a2ddd1f17f051ddd1f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 KB (37029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a839565c41a9f5e13e9da4f36948968b30038cbd861c3aad3216c20f4d4bda3`

```dockerfile
```

-	Layers:
	-	`sha256:2a840fea55a1939c9afcb14fb151ff38b3a4934a413b9658214d21e73aa2f6e7`  
		Last Modified: Mon, 03 Jun 2024 20:06:50 GMT  
		Size: 37.0 KB (37029 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:649e5a026812e45c1ee38fc1828743c640ec810140014c5533ed9e9a1f5453cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85443669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcaf325b146caf68b59fc311a96d0e7fde1e5e119967d5fc08f8ed88991a4c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=12
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=12.19
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=617e3de52c22e822f4f57d01d5b2240503e198a9eccaf598a851109bd18e6fbb
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13461a0b11d0afdd53d0436602eddc4ad89878a2ad40b64f0c4359a03b9d9dac`  
		Last Modified: Mon, 03 Jun 2024 20:38:43 GMT  
		Size: 979.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98fb215bc78e59d29bdad767e1ab4e8eea96fb261ffb0fcde16724b44ac745b`  
		Last Modified: Mon, 03 Jun 2024 20:38:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea48eebbf891f7eb918e843afe4d480d44058c89c7ea2556d290b8082a449a2`  
		Last Modified: Mon, 03 Jun 2024 21:33:52 GMT  
		Size: 82.3 MB (82333948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337fd8122f6d9441eeaaea8f504c13ce3751141930c8b723a1779057a8d283f8`  
		Last Modified: Mon, 03 Jun 2024 21:33:49 GMT  
		Size: 8.7 KB (8685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12015108509a6072bde9589f025e13f9cb2455ad6aef76aa6980008374dc9d92`  
		Last Modified: Mon, 03 Jun 2024 21:33:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e2616e458def123127e60a388740017907cd01d1255ae48f69918cf7c0a953`  
		Last Modified: Mon, 03 Jun 2024 21:33:49 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4afb375a2a5ba9c3b0813791bcd9c15f291e085978ccb6192724dae259eeb7`  
		Last Modified: Mon, 03 Jun 2024 21:33:50 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434df184ebef7da607878aeda4173f5f6e2a8557885350a1d164fc1f9ec9432b`  
		Last Modified: Mon, 03 Jun 2024 21:33:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:af4a0c494f23c2510f423cf45da754b4dca2e8116b57bfef99ebb2c1e87e273f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.6 KB (613638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4727184cfdbfbf21532d2e352fcc9add275c09f9d12a5985bfb3f733a6caee6a`

```dockerfile
```

-	Layers:
	-	`sha256:a342327a882ea7e97d9a49777210b9335ced6a4e46095875129de7c79db20bb8`  
		Last Modified: Mon, 03 Jun 2024 21:33:49 GMT  
		Size: 576.4 KB (576390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d309a4f0d1e4de427dd8c3871a39e38c558e07dad0732781eed9597aa6a131`  
		Last Modified: Mon, 03 Jun 2024 21:33:49 GMT  
		Size: 37.2 KB (37248 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:9b5933f83b8cf52e9c3cfe7b79d6d5f2610b1798d14a52f96124a5dcda1183b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91394650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2555e75544037c66ddc4e87afb3d16bd6d3818c58c36d087720e57162ab727b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
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
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948006db43269aa92582288adc4e7e014d1465ba87d4dc9fceef37dd98eeb800`  
		Last Modified: Thu, 23 May 2024 07:40:27 GMT  
		Size: 981.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5535d2d81d2194656bbe173ed89187952464827845c7e39cba2d14957729d0`  
		Last Modified: Thu, 23 May 2024 07:40:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51900132429fe7df7d1a6ea8ec9e90eaf9e3c15141d17f515cd90961ba58066`  
		Last Modified: Thu, 23 May 2024 08:30:53 GMT  
		Size: 87.3 MB (87292186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d3f0326286836d451cf55d1a98162b22ebe7d9f509d665502db8a4c698306f`  
		Last Modified: Thu, 23 May 2024 08:30:50 GMT  
		Size: 8.7 KB (8688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16c5c122eeb6d6de083500ad1ee0e575cb7c94951b0edcb3a691d9813a5e42a`  
		Last Modified: Thu, 23 May 2024 08:30:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20cd8d0bf6f4105ec13c7b7a123e2e6ddf015a1ef73d2c2b1f64fac4beb148c`  
		Last Modified: Thu, 23 May 2024 08:30:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eba6081be7943c1ba1763342b7dcc64acaa2075184e2ad2a55c5fa309e21c5`  
		Last Modified: Thu, 23 May 2024 08:30:51 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a646a68722217275cfbb19969607f7c3ea56cfbecb4cc64c48942f586bf5cc1`  
		Last Modified: Thu, 23 May 2024 08:30:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:7be5bc576ccbdfaf6a14ebc3cb9e1046b5fcf54bebefafde887d9abe12bc9ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.5 KB (613459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e70b5256ab844257f10dba6da82b3e8b009b4a5c6d575343c49c5f85f56bc7`

```dockerfile
```

-	Layers:
	-	`sha256:7ddfd3ba31cb9cab77f6a5e7486b541e193c3a1d248822757f557f16fab7fc11`  
		Last Modified: Thu, 23 May 2024 08:30:50 GMT  
		Size: 576.4 KB (576366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f7e335b51d71fa1a502ea8d4f40c0610c81da980b4b4c806c34bc4a95992c9c`  
		Last Modified: Thu, 23 May 2024 08:30:50 GMT  
		Size: 37.1 KB (37093 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; 386

```console
$ docker pull postgres@sha256:cc2991b0e5e92a444c07983685704a415d7933862fa0497a7347426fac21d698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97285247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1514997987025371bb0bbb95e1c928f818b3d28ff7d87bc73adcdafe69ed89b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=12
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=12.19
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=617e3de52c22e822f4f57d01d5b2240503e198a9eccaf598a851109bd18e6fbb
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6e23c12419cef0104bb9c7cf4d48b819c458547d64e601b05b2ee406a4ea26`  
		Last Modified: Mon, 03 Jun 2024 19:06:10 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9dfbdc19fa057ba2a700170fc5e34c5ee2cdb9f521fd3dfc3a870498c978c2`  
		Last Modified: Mon, 03 Jun 2024 19:06:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6caf7230a2e9a482aaa6a9778fce6b60d0528752f301fb7a0b8173e3df80b58`  
		Last Modified: Mon, 03 Jun 2024 19:06:13 GMT  
		Size: 93.8 MB (93802387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36040bc67816d560b9af96dab04210509420456e4de8c23a1f87f1d7cd10ff46`  
		Last Modified: Mon, 03 Jun 2024 19:06:11 GMT  
		Size: 8.7 KB (8682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0824f57412488c616fe19dafdf1a370a747ffd11628ff267bffa00506e5942`  
		Last Modified: Mon, 03 Jun 2024 19:06:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce401b5c9a409aadc02d6c839782d9c25f132929eb87ddb62cd5c9a570c0d9ee`  
		Last Modified: Mon, 03 Jun 2024 19:06:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25e7a523fed45c00cddef5902ce23065b0dd7940ea680130036f8f1cc5083ad`  
		Last Modified: Mon, 03 Jun 2024 19:06:12 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27af8827e1783447cda1bf6bc8e5af5c13961ffaf82855afb851d3a3c49b4c15`  
		Last Modified: Mon, 03 Jun 2024 19:06:12 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:988fb166d9881629388cd482721cc15df3fa0c9ce90ec1fb9f2add429d5ecc39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.4 KB (613388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bdc5677c2f68223f7ed3305e14255a75ce0f7fc86d0bddfea05362acb9a972`

```dockerfile
```

-	Layers:
	-	`sha256:c4d2b661994222f0d813080b14600a2ffb4363f46c824f96df910b3f7083b215`  
		Last Modified: Mon, 03 Jun 2024 19:06:10 GMT  
		Size: 576.3 KB (576329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfc9b4e269556e2e1e9715b0121560d12a86ca5372fd6f3dc29adb30894563fc`  
		Last Modified: Mon, 03 Jun 2024 19:06:10 GMT  
		Size: 37.1 KB (37059 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:7910ad69d035163884c9f303ba889b9871514f448c426a0f692198cb18f08db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96488471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bb0c00976996e6f13dbcc786bdc442c40d3b18b9e3eec646adf8e31bd31549`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=12
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=12.19
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=617e3de52c22e822f4f57d01d5b2240503e198a9eccaf598a851109bd18e6fbb
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fd1eee4c10ba5c208f6bdc0ac4fc73f2cbfadc9b2c92194411c012e4b9ac8b`  
		Last Modified: Tue, 04 Jun 2024 00:37:56 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2a6fa94842fa4d229e3c1c2c0afc9b3e7cf8bac75896cd4c7fbce3b0bb68aa`  
		Last Modified: Tue, 04 Jun 2024 00:37:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cfcd64bbe827c6e730adf30362cd44668ab87bfc9336d0d3ecea0e119c80b24`  
		Last Modified: Tue, 04 Jun 2024 01:30:38 GMT  
		Size: 92.9 MB (92902935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5c60c7a1f5f00ce7bdfee487b13fc874a24d7a95406bad6d478d42ab29e896`  
		Last Modified: Tue, 04 Jun 2024 01:30:36 GMT  
		Size: 8.7 KB (8687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d2f2eafda038d05e7497fac438e207b3bd8dfc55f909813a1b02e2aa893acf`  
		Last Modified: Tue, 04 Jun 2024 01:30:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3847f6e6b30e764290d8a87686ec1a5c629ae1f4ee9cde3a1bff9562b8208`  
		Last Modified: Tue, 04 Jun 2024 01:30:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc653049726759d02f380b618009d186d385e910fd0c2a68c81c2ca236452855`  
		Last Modified: Tue, 04 Jun 2024 01:30:37 GMT  
		Size: 5.4 KB (5426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518490a907720a2c0fbe8f3cb44e5ea3b9a4d948a0f3ca02be17f8b8aeb5fccb`  
		Last Modified: Tue, 04 Jun 2024 01:30:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:e981d56c05461c22cc04228912b85b88171f7be1820d77f376f4e6cc3c325aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.1 KB (610063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0200ad4c8067c3e022144d9bd3b96def2693da27d89a502becc685c93cefbf67`

```dockerfile
```

-	Layers:
	-	`sha256:a7eec5712bfd7192661623bdc7dbb0d8871bb9214c3cb06af9db0c6570dd1ce6`  
		Last Modified: Tue, 04 Jun 2024 01:30:36 GMT  
		Size: 572.9 KB (572913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:591935a6599487473dc4778d93c340574cfa7207c2293e047fc3541e6ee46c07`  
		Last Modified: Tue, 04 Jun 2024 01:30:36 GMT  
		Size: 37.1 KB (37150 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:c0c461b10dcfafaf5034742c9abd5d5a662be0a784aebfc6827e991be3f0e3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92209669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17804c1026534873c49398598a79044fcfb32ab4891ce59b2d5c92f1255bd84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=12
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=12.19
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=617e3de52c22e822f4f57d01d5b2240503e198a9eccaf598a851109bd18e6fbb
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397835f90d5b54bcf3350893c533d7f62222ce163422e08c4292b57e32932472`  
		Last Modified: Mon, 03 Jun 2024 20:18:07 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7681dc06ba012f91e87730fc72d8d4f0a1859d02a200495489016d5d487395`  
		Last Modified: Mon, 03 Jun 2024 20:18:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b9480a915185c3580c25f0d1271b6aaf913ac9c07944f861e1352ecee05869`  
		Last Modified: Tue, 04 Jun 2024 00:08:11 GMT  
		Size: 88.8 MB (88825407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56aecc529fd1c1b62b640d0ae8b8ad0fdfb295af7e5f303be5e590612eea21bc`  
		Last Modified: Tue, 04 Jun 2024 00:07:57 GMT  
		Size: 8.7 KB (8694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd9bc062bfc93a0766cd64c62bcbd36117ee1e07b068678d9dbdce644f25a97`  
		Last Modified: Tue, 04 Jun 2024 00:07:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4c5f9ee1529ee357064da92b4b76a5f6a6e87168090c1068ac474337704df5`  
		Last Modified: Tue, 04 Jun 2024 00:07:57 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfd464968e18c5947281fb6d5b06f81d1ae5d908dfe82999994f91c84161ccd`  
		Last Modified: Tue, 04 Jun 2024 00:07:59 GMT  
		Size: 5.4 KB (5427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f857a90f5ff918f3391e9ace902d9fd9d73804487ddd5e8c39bf58e287eac`  
		Last Modified: Tue, 04 Jun 2024 00:07:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:648118fbb04724ab04efa76577e4be5678e0f2e17ce74845571747727d03cf26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.6 KB (611580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d785cfffc3af493f1dec7daddcd7dc84d399ae189ed43919f604c96b5f1cc27b`

```dockerfile
```

-	Layers:
	-	`sha256:de8245faf062a89f50dcba44523ae30e9a122bf5374d9cfd146054cd6fc05ae2`  
		Last Modified: Tue, 04 Jun 2024 00:07:57 GMT  
		Size: 574.4 KB (574430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f675a4de78b3f89f636d82a58841725f063334e9099e1dbc1c44d3e46adc95a`  
		Last Modified: Tue, 04 Jun 2024 00:07:57 GMT  
		Size: 37.1 KB (37150 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:08810e30fadbd82994b53139ad2ecd995459c2c9cda6fc6d073565e5e8b4ead4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100779120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff67fc35d5a9662955d98f3b92e7124a9296e3789d5352a1ef984767f2623964`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=12
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=12.19
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=617e3de52c22e822f4f57d01d5b2240503e198a9eccaf598a851109bd18e6fbb
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f17f8c990c0ab5858469098b11d092d504ecbf4970fc3447a12f12e8acbfab`  
		Last Modified: Mon, 03 Jun 2024 19:51:51 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1a12ac87f16915117c6298db53620efe1c42e9277ed1b5b851ac46ffc57bd0`  
		Last Modified: Mon, 03 Jun 2024 19:51:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e66b3cf39bc1497f9f4aacca43b8280f9336e34ddb928d29b1c377a75a20bd`  
		Last Modified: Mon, 03 Jun 2024 20:52:34 GMT  
		Size: 97.3 MB (97303090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae80129f18c80fb1633a7afbeec8f00fdff49aff4a73f797a7f9958388725db2`  
		Last Modified: Mon, 03 Jun 2024 20:52:31 GMT  
		Size: 8.7 KB (8688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b8b25c4077aeefcbf2d878feecac2655ba927214d17ee44a6c0331ad596f8a`  
		Last Modified: Mon, 03 Jun 2024 20:52:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48a8b1c3561679e08885267bc96b35bafb8462ecb5f04af5f518b35f4f67e33`  
		Last Modified: Mon, 03 Jun 2024 20:52:31 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26946999ec9d7fea713ee2dab8e92a30cebff6fc2e3ed1e9d47ee2624881c4e4`  
		Last Modified: Mon, 03 Jun 2024 20:52:33 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ea45f70b5c18e23b3ce5e811881b4b523ae488c514e0f17c2122d18459fc7d`  
		Last Modified: Mon, 03 Jun 2024 20:52:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:d3e57e6b7f466aad6bc4f49894e20a2dcf0c7d00379e68f7c13da12c9dbba3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.5 KB (611500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff8068769e239d985c48bd1a7aac498ead9797eef4f640ea07c98df4ccc83d4`

```dockerfile
```

-	Layers:
	-	`sha256:4dab479798a7f356b3e7a35fda651786d2fd3c038860a6500044fcf681047f4b`  
		Last Modified: Mon, 03 Jun 2024 20:52:32 GMT  
		Size: 574.4 KB (574400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61b5b3277e79c62433a702caa0490667e9f92048c8151636cbb7dc95130b793d`  
		Last Modified: Mon, 03 Jun 2024 20:52:31 GMT  
		Size: 37.1 KB (37100 bytes)  
		MIME: application/vnd.in-toto+json
