## `postgres:14-alpine3.20`

```console
$ docker pull postgres@sha256:55f598cbc036eace97251d36add56bf2460e60d705a76c2f0d6f63ace976e733
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

### `postgres:14-alpine3.20` - linux; amd64

```console
$ docker pull postgres@sha256:6893f95b4e054d0c0b9a39561f830315f7a421b97526a108ccbfc797214f8f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94226671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4b6c853070e3f662255406b9cfd1ed63b030bfc3fe5606728a917da12419e0`
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
ENV PG_MAJOR=14
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=14.12
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:57103dbfb65d02189c946990edbdd4dae7949d1e8b6e340662a959dd641c1a4f`  
		Last Modified: Wed, 22 May 2024 23:59:21 GMT  
		Size: 979.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ee2744e27dec40e8efb459975aeee6a069a23b10578052acb9e005b75e36bd`  
		Last Modified: Wed, 22 May 2024 23:59:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3062d5befd91043da4a7c2d3825fd19025ba575a4449feff655c15b08930791`  
		Last Modified: Wed, 22 May 2024 23:59:23 GMT  
		Size: 90.6 MB (90588377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a75adef0046588c0811953096f39d28a93a9744ea7ccfc54a7e2926cbd1f3b`  
		Last Modified: Wed, 22 May 2024 23:59:21 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f734eaee16fbafc376814e70237da61d812a12e0e270f4843551c8d70530f7e`  
		Last Modified: Wed, 22 May 2024 23:59:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c45bbf7601ba056776698c50c04cf4147a55fe6d9a86d4e46ee226851894833`  
		Last Modified: Wed, 22 May 2024 23:59:22 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83adffbd3816ad6b04a2e2a3ed86986a0a7085477ea29da56a906a7a9723cf73`  
		Last Modified: Wed, 22 May 2024 23:59:22 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d26101c9ba0327762e271c5c5c7b2ca289b96a071db0fbe8914331f1c952ff`  
		Last Modified: Wed, 22 May 2024 23:59:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:2599e75d8eec5383291d0dafc9368b0ef296a53702041dfcd6ecf423a99757d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.5 KB (616547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7a6281c2950cf8eefc3fca0c6b470b9b6f89460c0ccfc5513ca1439fb65a4a`

```dockerfile
```

-	Layers:
	-	`sha256:b4be48929eb793ac415ed86cc07de8d0387e90f9b951c8abb41a5fd0a82c84fb`  
		Last Modified: Wed, 22 May 2024 23:59:21 GMT  
		Size: 579.0 KB (579017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890c79179ea68a052226d2ccaa60eb619e3e7dbd353577afba20772c8ad04377`  
		Last Modified: Wed, 22 May 2024 23:59:21 GMT  
		Size: 37.5 KB (37530 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:794443d5540b2bf6ddddf4389541147f27527ff821e72f607ce62043dce1f4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93021122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b47a761947bbc69c2fa018412a1c901d6034b6df087b683bf6cdbf40530eefd`
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
ENV PG_MAJOR=14
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=14.12
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:e4b23e3e1677cf5b991fdbd920205f5892f95ae3c45bd58b819aa3d7574705d5`  
		Last Modified: Thu, 23 May 2024 00:10:58 GMT  
		Size: 89.6 MB (89639870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93df52631e6c1cd8ecb9859043e1a80f290faf0e38fb320be1151e81cac8a3b3`  
		Last Modified: Thu, 23 May 2024 00:10:55 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01afca5c2c500f2f15613f83ebcf92decabb657868c25980ee58086803e7787f`  
		Last Modified: Thu, 23 May 2024 00:10:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5067245f53fcfb9a7b3407407c4433720c7ffc248fee26fb17e6cbb715cf52`  
		Last Modified: Thu, 23 May 2024 00:10:56 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443bbe286dcc50b20bb8016dccb45d1652572a59a344ffa01d12e27256618b66`  
		Last Modified: Thu, 23 May 2024 00:10:56 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aab454f1a31a227d4195eafc3a02801e0ef56a71d6ebdf4bf99a3b0e35fddc`  
		Last Modified: Thu, 23 May 2024 00:10:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:a0cd9350f4ef27de26c3a186c0490b113f82e9de111b254c68c4e8eb75babc93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 KB (37294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be1694b2cb9ad0ddc6e7aa39d7913e2263fd1de000e280436753341467b89c3e`

```dockerfile
```

-	Layers:
	-	`sha256:d60bd91bdc2a1b0b6cb67652c259d9cefb8e83dfc0b51eafadd1e43b51223348`  
		Last Modified: Thu, 23 May 2024 00:10:55 GMT  
		Size: 37.3 KB (37294 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:6621dbdddc36b041159de7151f127011c8fc14405940837ae36475b0ffebed0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87466016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2e93899cee7b94f6dd56f3e1b9fa5a81251ce9f762480afc47d9afb893b89b`
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
ENV PG_MAJOR=14
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=14.12
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:61bb2b4cd68ad872d98ec52f18cdfa2f034afba9a031a14912c0012e7e6dc0aa`  
		Last Modified: Thu, 23 May 2024 01:09:44 GMT  
		Size: 84.4 MB (84355779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15771d6769c47896246ae4bd977679a5b586b9780c3251b5974014313bae5d14`  
		Last Modified: Thu, 23 May 2024 01:09:41 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3c58ae380879727c5ded6141a69bce3e36ab8da7e49724c758f45a4cdcb129`  
		Last Modified: Thu, 23 May 2024 01:09:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd88572ed373b28d40987ff4bdca69e1cd98af35f2465589becf7c589163d2`  
		Last Modified: Thu, 23 May 2024 01:09:41 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1a2068001de1950cf90bdedb05f43c14aec570346cc01615db1bda25e61536`  
		Last Modified: Thu, 23 May 2024 01:09:42 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fae28157dbbd3f25ab7d83646f3ddfad026ff2bdd3007f3c0303e73b9b0d44`  
		Last Modified: Thu, 23 May 2024 01:09:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:8161edd7a9ffc14b90ff01d4c18ecf9a75e20f9fda87ea1f72a74c6628ac476c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.6 KB (616566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8c70e564ad5cd04909b63736626bfcaf0bbdb2ced19872037bf81b028c4003`

```dockerfile
```

-	Layers:
	-	`sha256:9d2524f7756a9937f91dc4cac74eeb4ad113e779a5c3d00e886b1f41e5c72c81`  
		Last Modified: Thu, 23 May 2024 01:09:41 GMT  
		Size: 579.1 KB (579053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ebdab5f13cb8dc62e3c756813da0cdc069f824d45b03ce3621e26519d06686e`  
		Last Modified: Thu, 23 May 2024 01:09:41 GMT  
		Size: 37.5 KB (37513 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:d8fd8fa637b063be914c4bceb1c7ccb16ed33b333e06c3ecc65792083f7a015b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99565470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5481e9c813986e1a232e2cd47d5debb919671af160541ea30d8e915066aaa94a`
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
ENV PG_MAJOR=14
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=14.12
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:7cf504f61f42b4d4a604591850e7251e6654bc026cceb57926a4de752cfba80e`  
		Last Modified: Wed, 22 May 2024 23:59:30 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b22fa4e90da4dc4cce5bf74b5d1b953acf5511149e44761f45f9a05e74cd82`  
		Last Modified: Wed, 22 May 2024 23:59:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2125087fe1859cde9f6d7544ea381bf71d34051defff946c716169850aa8dd7`  
		Last Modified: Wed, 22 May 2024 23:59:33 GMT  
		Size: 96.1 MB (96082097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7fe68be9852bb91fc28d4bbca69c6b1b3c4e07012163d99da78b00979e439c`  
		Last Modified: Wed, 22 May 2024 23:59:31 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6c24d149f5f0459582d672fb5ed618264f357f788a1908ce2b4f1a14f92d73`  
		Last Modified: Wed, 22 May 2024 23:59:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9083efd4e4c9605109b0548aa2918d732485674fd6d428978bb43f24246efbc`  
		Last Modified: Wed, 22 May 2024 23:59:31 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbb5e8fb61e5b5c5ea850e06cef1e7f6f405d480a12423c4021e7acab6b001a`  
		Last Modified: Wed, 22 May 2024 23:59:32 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b1b9e062a0bd6f591a6085342426d5f84aa7c200078f7c16c68024e1158e0`  
		Last Modified: Wed, 22 May 2024 23:59:32 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:78b3b68ab56247ba4d9ca7d7532974b62733aa7d4509c2261d3e76a4d3e7056c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.5 KB (616481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d74f7466a768fc23e4c895ff8402f7e1c5edbe0fa83288204f754122ef08b0`

```dockerfile
```

-	Layers:
	-	`sha256:f0a0f5a5ce54be8ca5155f7688f591f28e79e578e54f3f17e2515e929e32433d`  
		Last Modified: Wed, 22 May 2024 23:59:30 GMT  
		Size: 579.0 KB (578992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:232c4380d10050a3944b9b2927347932572ecb39e75c687c53e878b3c3b17d7c`  
		Last Modified: Wed, 22 May 2024 23:59:30 GMT  
		Size: 37.5 KB (37489 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:43cdc7c1220ae819d3419991c4f0681ba14f31b0e5c6353844b2e3dc029467fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98804660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc75e8c8a9efeded4f464d3cc527f4f139fa14b91e223b64cdf76b9463ed8f1`
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
ENV PG_MAJOR=14
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=14.12
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:cfc23fca64a35c86a4f86de7da499c64a052ef39467f6348404ac12ecc91dadd`  
		Last Modified: Thu, 23 May 2024 00:48:15 GMT  
		Size: 95.2 MB (95218608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9877093f2d3cb54d5e806e586428fe261bc305b391fc3f104f0de907295706`  
		Last Modified: Thu, 23 May 2024 00:48:12 GMT  
		Size: 9.2 KB (9208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06172092464d2dc54760f151006f7486bd817cd725cec5c6ebb051ba019de456`  
		Last Modified: Thu, 23 May 2024 00:48:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f8da96be265ef4397e58c98f158371196a0e0ced3c9da41f386b13f87ef14`  
		Last Modified: Thu, 23 May 2024 00:48:12 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f21af19386d17a294fb60439bd5f6e14089c5b6bee70c8e5bebe3c9290c58e`  
		Last Modified: Thu, 23 May 2024 00:48:13 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0089359ac520159a64ace77d9fb7c8b4f27f8d504aa84081fc83458dc42ed030`  
		Last Modified: Thu, 23 May 2024 00:48:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:ac11c22fe65657a98b895dbee81c2643312608ae5c4fec7fd83aaf4a13e7377e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.0 KB (612991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb5df898b7ac063efb56f36bf6f47123ca4b3982ab441ec2382aae3a5fbe5ad`

```dockerfile
```

-	Layers:
	-	`sha256:c8f0827ffc44a744b9512e74b681397c7fbd2b95200428c71be94da867992c98`  
		Last Modified: Thu, 23 May 2024 00:48:12 GMT  
		Size: 575.6 KB (575576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc4e5ea3507f1e92dda7be4f09d79c0d5693fcf6de276dc9d6d34a3178dd056b`  
		Last Modified: Thu, 23 May 2024 00:48:12 GMT  
		Size: 37.4 KB (37415 bytes)  
		MIME: application/vnd.in-toto+json
