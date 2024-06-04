## `postgres:17beta1-alpine3.19`

```console
$ docker pull postgres@sha256:202edaa621c68c4855b039dd3d8686197cd681743b6a1780f25d8e8eb37c4b2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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
	-	linux; s390x
	-	unknown; unknown

### `postgres:17beta1-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:dbd70fa84eb6f6ca37232d50e91f36738fbaf6572e417fb0d058ea105009686b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (99027431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bad7b7c9696e9515f102b31e02dc6e73059a9a31550dccca0025d7737d44811`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=17
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=17beta1
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=089e8854fecd0ca1ec5cd8b29526938f9ef5e91cc331f5d6e118d13468f08f50
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912625c3f1749211a9ec388a6614b831ce8dd939053927f543aeda8b3d1a1a12`  
		Last Modified: Mon, 03 Jun 2024 19:06:47 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8cc0030762eceb5692ccda194842bb81aff910f2e9b05e9915463707e5e6a7`  
		Last Modified: Mon, 03 Jun 2024 19:06:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513e02b298b213920e50422e8edd014a2f6e917249e2293b19fcd7d417fce40f`  
		Last Modified: Mon, 03 Jun 2024 19:06:50 GMT  
		Size: 95.6 MB (95601524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647d4b69bcf245e727b3577603447abf9a04e6cd21b3cc94eac1ab0e5b774629`  
		Last Modified: Mon, 03 Jun 2024 19:06:47 GMT  
		Size: 9.9 KB (9889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45dbbfa810f150c2997a1cee8bdaff5025d87dd033a2884f5af16987d62ab91`  
		Last Modified: Mon, 03 Jun 2024 19:06:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df724fcadb81e8def27956b7d11a61196829a35ed84b2c65f72728702b3bdc95`  
		Last Modified: Mon, 03 Jun 2024 19:06:48 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ba3adc701e0fec762bf5fa5b185c3504466951b211a9ac159d0453079f00d5`  
		Last Modified: Mon, 03 Jun 2024 19:06:48 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef5f60b28d40040baaa6339a685a840e3043a0aed819944dec5f3e1aaff518c`  
		Last Modified: Mon, 03 Jun 2024 19:06:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:93bb79d4e3d6380b968b6ebe6d7e01f4a26d38bb7c97bdea6aaf27764ccb4d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.0 KB (992989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916a4ad1869a3bb66972a853aee2ec4967f235c25aeca14b9bd00300111a3852`

```dockerfile
```

-	Layers:
	-	`sha256:605590345ebe4596c567641c90843990e831a5841543bf32b6452b0d2edf00a7`  
		Last Modified: Mon, 03 Jun 2024 19:06:48 GMT  
		Size: 956.4 KB (956386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714b8c83c33738f51b13e774021f172f81246f2c097a405361cec59ef343bc09`  
		Last Modified: Mon, 03 Jun 2024 19:06:47 GMT  
		Size: 36.6 KB (36603 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:cd39a82960c8a3b7867870d2a51e59d84de29a8e46f516203ff4c07d8923e095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97393508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68aa94b067320068886b8ff61aa5899a5e91a6698b28f3124ff5031aa2e9ebfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=17
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=17beta1
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=089e8854fecd0ca1ec5cd8b29526938f9ef5e91cc331f5d6e118d13468f08f50
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860e35ae27435bcb376652f33da561573efc82cb903cc30ce3684aff0ca6d38b`  
		Last Modified: Mon, 03 Jun 2024 19:26:27 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a305f8be1993a674347a47e4e4da6dc04c8b7969a73d6830b0cfe4e8de939888`  
		Last Modified: Mon, 03 Jun 2024 19:26:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882ae644e5ba75824bbaa6f2d94818deb29f999c34a7920b2c65077c3bde2809`  
		Last Modified: Mon, 03 Jun 2024 19:26:29 GMT  
		Size: 94.2 MB (94210935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc64159a0a9de2422a4ae13752c022215b568deb2a549be85d7ca03af3d330`  
		Last Modified: Mon, 03 Jun 2024 19:26:27 GMT  
		Size: 9.9 KB (9892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fee33f5e0ec1ae7c8c32aa3b4cdfa4688c9449f91686c1b39d11ad689c53f2`  
		Last Modified: Mon, 03 Jun 2024 19:26:27 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164f3113b1d738933b39a7c2d9ee31ea6b76adf2a80be3f01f9051b635a0e329`  
		Last Modified: Mon, 03 Jun 2024 19:26:28 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1566eb255d5860eb089611e0edeab447b1456d6745b3617f291b70d4a0971bb`  
		Last Modified: Mon, 03 Jun 2024 19:26:28 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5542034d91d012452d4e56024f544942ac1997b9bf67d78b1b4823f6c1c8e2`  
		Last Modified: Mon, 03 Jun 2024 19:26:29 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:bfe2a4a97a681337d8cbf703d25c2203f822875373662c4d38a6947e78e5490a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 KB (36508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89bf43a9266b90a637b702c4f819b8bcc70d7a67744cf892ee1f7e85d1b1b3e`

```dockerfile
```

-	Layers:
	-	`sha256:b24f4749ab2f1c29f1f173749c574accf0678b38b3ed3f56a5dd4ebc440af840`  
		Last Modified: Mon, 03 Jun 2024 19:26:27 GMT  
		Size: 36.5 KB (36508 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:80c894e12a60c49c91428aff31b32fce0ce1f1f3df868c368c3daa8bea626b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91681091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd743fbd633bd60d207ebea2d8c105ecf8b1984db11f83c42cf17f357a764460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=17
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=17beta1
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=089e8854fecd0ca1ec5cd8b29526938f9ef5e91cc331f5d6e118d13468f08f50
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e4bfd7c0deff5a703442b05eea3fc3238bd197ba703ae949a0a735a738790f`  
		Last Modified: Mon, 03 Jun 2024 20:42:33 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6f980339956e09a15f739f93841e0d33b8e50c83f4e1c2c83dd4ead7ef7a6`  
		Last Modified: Mon, 03 Jun 2024 20:42:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3777522a14be6a517a2a38d3ee06d9f35976ae55c0ff4211953b0becfab2f975`  
		Last Modified: Mon, 03 Jun 2024 20:42:36 GMT  
		Size: 88.7 MB (88745013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0140d2f1ac6faa1c27adede34ca1b7668caca7f2e752d0d13d87f5a75d909af`  
		Last Modified: Mon, 03 Jun 2024 20:42:33 GMT  
		Size: 9.9 KB (9891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c374ff3f7973f01cccfa993a9694608247662a006cf3c200a6e6f48751cd20cb`  
		Last Modified: Mon, 03 Jun 2024 20:42:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb2dffaffb1d9c11a45bfec853fd19d07acc8bdcd4658d7166e72049f9d18a2`  
		Last Modified: Mon, 03 Jun 2024 20:42:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fbaa5eb5ece366f35f5cb67c6040d493a8e5007093e9ff3790df9270f347af`  
		Last Modified: Mon, 03 Jun 2024 20:42:35 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53621a8ddb6b912c455e48d0b95ee3f2c8f05ca4ea4c92fd24321884af28ea3a`  
		Last Modified: Mon, 03 Jun 2024 20:42:35 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:0a4d080e9104f605be3fb9d0c8fa6df05bfe25616b9ae0ce35dce9a0d7736f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.1 KB (993125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7799a0fbaf5320bb511ac251e1bb1f20512bf14e0dac07e382ee6d881e0f0f54`

```dockerfile
```

-	Layers:
	-	`sha256:cd7d27fdae09193ac860d914962974516a760a369d65d5b75d471b85d549fe4b`  
		Last Modified: Mon, 03 Jun 2024 20:42:33 GMT  
		Size: 956.4 KB (956398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90946b3983c85ad7305924077bd9b3c4e84782b7b1c5b8c8fddc4b4bb0ba047b`  
		Last Modified: Mon, 03 Jun 2024 20:42:33 GMT  
		Size: 36.7 KB (36727 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:c5c05907a5cee4bbd38eff71f00c5593e70c317c14585bb8d81eae01e479048b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104192486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a949e418abe83152ae28873a6c51f7353d15bd9525df15c70ba92604a89d6af3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=17
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=17beta1
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=089e8854fecd0ca1ec5cd8b29526938f9ef5e91cc331f5d6e118d13468f08f50
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289c73ebd6e9a5aa05d4aec41cf54524d64c4157ef945757109ff17faf6b5d71`  
		Last Modified: Mon, 03 Jun 2024 19:07:07 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9dfbdc19fa057ba2a700170fc5e34c5ee2cdb9f521fd3dfc3a870498c978c2`  
		Last Modified: Mon, 03 Jun 2024 19:06:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a03f72f38a08ef4adf5379874aeafdc5dbcae716ca8c122dee9bf4b0ab008c`  
		Last Modified: Mon, 03 Jun 2024 19:07:11 GMT  
		Size: 100.9 MB (100931220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb6d1c380e9120529f1943853006038d1450adc5c615d45d5a886d8d96cbe16`  
		Last Modified: Mon, 03 Jun 2024 19:07:08 GMT  
		Size: 9.9 KB (9890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48720c65e7b2f752533bb1aac70e552daec0a7e36cf12ac8a5a22559efe90e4a`  
		Last Modified: Mon, 03 Jun 2024 19:07:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3667f32b9c4848974e9d4625538e2b85eb8d1f01f4538241f7f734f01183f58`  
		Last Modified: Mon, 03 Jun 2024 19:07:08 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d92c94a5bde60df3729fc55b38bd29301d455149dda908a06b8e83ff958b4d`  
		Last Modified: Mon, 03 Jun 2024 19:07:09 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8684ebd11be03d9cb3cc70179b9a5590a9765f0c2d8158044cbdc2de305ead97`  
		Last Modified: Mon, 03 Jun 2024 19:07:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:ca045d3703615d7bbe4fcd388512a8e1fb21c36528d55d70ab6322fecd916daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.0 KB (992958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21bc5ca29aa4a158ce1a400857a938cc73376837d94130c6f0b67d375dc4e18`

```dockerfile
```

-	Layers:
	-	`sha256:f7f831d2f1e422ed9a758c76ff627b8fccdb500f572c87ced5905de7a746edca`  
		Last Modified: Mon, 03 Jun 2024 19:07:07 GMT  
		Size: 956.4 KB (956376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d9bee6eabad6e065a63122ff3109a42bb16e3aa74074144aa743cb3d0ae4e30`  
		Last Modified: Mon, 03 Jun 2024 19:07:07 GMT  
		Size: 36.6 KB (36582 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:933e57f6e47e25c7bd8bbaaded630064603c2066dd08fde7c4a900791d92a845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103596888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b6a2822ecd6b3661c76c3a515e513ffdd0da16a6a1d10b3ae364f440cc5dbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=17
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=17beta1
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=089e8854fecd0ca1ec5cd8b29526938f9ef5e91cc331f5d6e118d13468f08f50
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc0a98c9d584f2a67805c2d06416946139d1fc100fbde03f3fb69498d4adc87`  
		Last Modified: Tue, 04 Jun 2024 00:41:59 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46b4079b8ab65d67e0592c39b5171188bfa6367e02f4dd92f69cdf45d9ce755`  
		Last Modified: Tue, 04 Jun 2024 00:41:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac40b7275d1faf40be83f0b786ce25aa46884cae71385269eea0501602dc69b`  
		Last Modified: Tue, 04 Jun 2024 00:42:02 GMT  
		Size: 100.2 MB (100221346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277a93ac4bf2997d00bc05b0053cdc34cd89fa0850efcb5048c4e977670d427b`  
		Last Modified: Tue, 04 Jun 2024 00:41:58 GMT  
		Size: 9.9 KB (9900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cff1fba15705698f6afa274744a7cf24c0dcfa99b62f90e081ea6954f28359`  
		Last Modified: Tue, 04 Jun 2024 00:42:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48c3c4cc754980ead7583e703b7b955bdf55ddb08ab17988d2deb00d4fcef48`  
		Last Modified: Tue, 04 Jun 2024 00:42:00 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e01a576071285d931390880adf69965b1bb67e29f159a279ce54efd5da4858`  
		Last Modified: Tue, 04 Jun 2024 00:42:01 GMT  
		Size: 5.4 KB (5427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72cde4a37d14abddeb8b4fd2bc4eb6ab20ee1a976d01da5e0d846d7fde003ef`  
		Last Modified: Tue, 04 Jun 2024 00:42:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:3b2314e90edf75a863b3ea93ed42d23246826ad7fad75a792bd0d0ec977451cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **989.6 KB (989568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea9f3a9748744b408f836c6bcea9962247383575a6f091c37cc9a6a099d1925`

```dockerfile
```

-	Layers:
	-	`sha256:38354f6e9bd82a5d1388a2c47994e3fe8326f0c3de357af7988d496bcd9ff010`  
		Last Modified: Tue, 04 Jun 2024 00:41:59 GMT  
		Size: 952.9 KB (952927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efc9d087a00b4627909102373b69ac84962b6593b178a23a429e2eda3892e618`  
		Last Modified: Tue, 04 Jun 2024 00:41:58 GMT  
		Size: 36.6 KB (36641 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:d4c9f2a3ba713bbc6a597cd6aeb3728919e66cc119f72e0162d94116d368cf4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107718237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6218bd14c3e0f509bd9051e419d24be1fd4fbb694090848e67b16853324a7e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=17
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=17beta1
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=089e8854fecd0ca1ec5cd8b29526938f9ef5e91cc331f5d6e118d13468f08f50
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddf070e1afb1dfa2858898d44cc73300f9c817c9455e866395af0ebaadac77a`  
		Last Modified: Mon, 03 Jun 2024 19:55:56 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9d3e69e197d6e0a5091fd3be948bac07f0cefefb29f336d0fc54d6ba476000`  
		Last Modified: Mon, 03 Jun 2024 19:55:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07817c6e4d4b96fb702a0f04dca87ead02e9821ee500f59f0a07172031148750`  
		Last Modified: Mon, 03 Jun 2024 19:55:58 GMT  
		Size: 104.5 MB (104458422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ffe3c3920bd1cde3e9401804d8ac3671d9910084987c10dcf1f46f08c3fbd3`  
		Last Modified: Mon, 03 Jun 2024 19:55:57 GMT  
		Size: 9.9 KB (9891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211b8b92cdd3f39fa3b64e63d6b15e9ca711872944e336a7ec307f86c97aee7c`  
		Last Modified: Mon, 03 Jun 2024 19:55:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbc89150285a5b6db2f05669f7d60909803bf34a52347e58aef961f33099931`  
		Last Modified: Mon, 03 Jun 2024 19:55:57 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4615e1cb06fbc82030a7774ccd9f6b91c23e644a04f2b15d37d566dd18eeca`  
		Last Modified: Mon, 03 Jun 2024 19:55:58 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfedd980b84d7b7ac8660ec3e9664eaaf5ceaa16c4e6760294d065a41db128f`  
		Last Modified: Mon, 03 Jun 2024 19:55:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:172aae7728b889df6bd61ff1f9c7cf7c9824581a8550e823f513dfbaf10cd729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.0 KB (991041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2c65a9df377c38e3385619ab2523b4121146fce6e1ca1446f1d1611a061a6b`

```dockerfile
```

-	Layers:
	-	`sha256:f68bd937ffce7b2dda5e05a679a2501684915aff9aa3e08865ffdac7f258d8e8`  
		Last Modified: Mon, 03 Jun 2024 19:55:56 GMT  
		Size: 954.4 KB (954432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4de64788a7f486276ef61b5a61707b05fc11132a98ae2bb26723d32d4a801226`  
		Last Modified: Mon, 03 Jun 2024 19:55:56 GMT  
		Size: 36.6 KB (36609 bytes)  
		MIME: application/vnd.in-toto+json
