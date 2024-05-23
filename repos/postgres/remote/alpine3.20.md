## `postgres:alpine3.20`

```console
$ docker pull postgres@sha256:34962e4b6f636c5eac3f61977e6c1ead79449782406e7c265ef20be0d3ee571a
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

### `postgres:alpine3.20` - linux; amd64

```console
$ docker pull postgres@sha256:7240c6a7165b2cbedae31f07368dfcd3bd5180455311fd4a8df522134dad4a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95742473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97701858621e6e9afa18032a666666e52dc38e42737c2e2136b595a08c80e4d`
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
ENV PG_MAJOR=16
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=16.3
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:d29578debbf7a0ef3e85b7a068c7e097ade772864869eb74a860eb18c1f74ce3`  
		Last Modified: Wed, 22 May 2024 23:59:41 GMT  
		Size: 92.1 MB (92103822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb83e095c2c596b6090af6e44e21df12520bbf9dc9a097e829483c821b32d483`  
		Last Modified: Wed, 22 May 2024 23:59:38 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce15d92d22a2ce038b7e9ccd8562a0815c4a39132303464420e7e705196d44b`  
		Last Modified: Wed, 22 May 2024 23:59:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a493f79a7a56f0e4aaf3027784c73964ca6806903c8d9a4fac8292ec6498f1`  
		Last Modified: Wed, 22 May 2024 23:59:38 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a11e3af9edf9b0c06d1fa25ee60c9ecc1e21ccd17f4b0eadc920cb6e1997ea6`  
		Last Modified: Wed, 22 May 2024 23:59:39 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74f8aaae0d08e05fca0450875e0e8be17fb516a242fb3e643bed7d02198ffc1`  
		Last Modified: Wed, 22 May 2024 23:59:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:bf683716e23bf307c6bf79ce61afb67fd9d32c888ad1dfe076670975ca15e8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.0 KB (617991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05face2216ff41b076ca654cbca7034e2c5273e854fca604fb5978db6957431a`

```dockerfile
```

-	Layers:
	-	`sha256:7ffc5b9df55f6fbf1bafd39a6369e347ade1da5cee0cadb6b8030a3cc22b6a8d`  
		Last Modified: Wed, 22 May 2024 23:59:38 GMT  
		Size: 579.6 KB (579623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dad564086dbabf8a3f1b4320e44abe79b9fd567ad7ec275a55be41f23d991334`  
		Last Modified: Wed, 22 May 2024 23:59:38 GMT  
		Size: 38.4 KB (38368 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:eae540dd7897b0c818023570db6885e666a4f8c038e46dcafe77c2f22a4a4b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94485955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b5997e0f92a3784529160a7b270f4df3bb7affb0e27d994089f731051ce948`
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
ENV PG_MAJOR=16
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=16.3
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:0ed47d305bf73d534ccf550a967a7199a31d1f5d9f08d37341642dc2099e189c`  
		Last Modified: Thu, 23 May 2024 00:04:19 GMT  
		Size: 91.1 MB (91104341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b384384a07f6512602767014606cea23dab26c1cc215e3038c6ca441aba8280a`  
		Last Modified: Thu, 23 May 2024 00:04:16 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41008ef94694f00d1521adb084985a75bcf6fcdd985e236a493cfa349255ec4`  
		Last Modified: Thu, 23 May 2024 00:04:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7055b09e77f937aaa9b19a021f261500615239d412fa198e0a5708f60b9fb5`  
		Last Modified: Thu, 23 May 2024 00:04:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e42fbfa8fdf264c3513b026a2741749dbdec68e2f5377c33afe33e14704566`  
		Last Modified: Thu, 23 May 2024 00:04:18 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e9ddf4e239c1d888f4213cbf81555a51ca150fc2e27679894f2c62752ab229`  
		Last Modified: Thu, 23 May 2024 00:04:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:c31c7e51f8037732c6c7ee28af13065c6dcc9dd32b7436df9975266ee484ddaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b7f74248d7011c78db1e5055bbe20e87781be0df78fd8a257bdcd315e9c0ab`

```dockerfile
```

-	Layers:
	-	`sha256:669217df66e476ad76c2b7815ac8e17e05802968e533f1f098b7c68df1e7f11b`  
		Last Modified: Thu, 23 May 2024 00:04:16 GMT  
		Size: 38.1 KB (38147 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:054083d1d11a702e6ceca555b0674547234261f12f92c7932fd00434f27c62b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88895466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b5fd468b9c17ccce99828873f16bfd71a8904c5a3e528455ad856d0dc34cc6`
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
ENV PG_MAJOR=16
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=16.3
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:f929e0c800818ab78fb3d5a0f59de1aaea898f09fc0c7687fb9a9b696c9bf0e1`  
		Last Modified: Thu, 23 May 2024 00:47:48 GMT  
		Size: 85.8 MB (85784874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a99297d963477789ba981c508d14a51dcef0cf1bd6febe285b0dd04d7c3ac9`  
		Last Modified: Thu, 23 May 2024 00:47:46 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168a7a7fa488c9be25698f07b17020065f35dcff8465452beb87be1df613063c`  
		Last Modified: Thu, 23 May 2024 00:47:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605716897df90597b6f13387720c4d0690e17506215d751908ca71141e62cbac`  
		Last Modified: Thu, 23 May 2024 00:47:47 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4103233ebf4c594a73ee55d963c0a1ec1315cde67b687cbf7837d8e161115b1c`  
		Last Modified: Thu, 23 May 2024 00:47:47 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3269199639314539c8b4dce69c69b2c2fc815396e2758d105841bdfc52c4eb41`  
		Last Modified: Thu, 23 May 2024 00:47:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:852009cbefa5d71c0100d4eb91be78a4aaff520d0a525c08d374e977e61bf790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.0 KB (618042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709185b76973088c279c702b767356563065f25d3093b39938ba3b300fb5a8c3`

```dockerfile
```

-	Layers:
	-	`sha256:6c91ddb0dcc6f35b31d2fe0ddb69f8cc7dd7aed536e56fdb758e5be0fe30d47d`  
		Last Modified: Thu, 23 May 2024 00:47:46 GMT  
		Size: 579.7 KB (579675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:271bbf5f1e48f4db2eb590bb380b5858820d7b70a4228ca4a260c9ea6faddb2b`  
		Last Modified: Thu, 23 May 2024 00:47:46 GMT  
		Size: 38.4 KB (38367 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:7a0d62e6bceddd811ea3241017244eeab50722504c96f789c00b67512a8b54ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101080541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e8fc0e2a7be0df7a9f1da2df6a9dd5d0571318066e546e3d05f56be2f9cad7`
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
ENV PG_MAJOR=16
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=16.3
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:32906906e10704a4b0a7c796ebbcc362e7652cc8cd2f92b4ada1f2ddb8acf473`  
		Last Modified: Thu, 23 May 2024 00:00:12 GMT  
		Size: 979.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03209e5f92584b8a337a7cd26e75f8f640f68fde6bafbabaacd6ea5e34de4886`  
		Last Modified: Thu, 23 May 2024 00:00:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ffffdf6399bce18f47795cc66bc191bc6f07c8a18a4b82d4ff45b1ace07c00`  
		Last Modified: Thu, 23 May 2024 00:00:19 GMT  
		Size: 97.6 MB (97596801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae1b65aa9de525620ef712f451b81d1d4c9b7009768b56644b0dfaf8ad646fc`  
		Last Modified: Thu, 23 May 2024 00:00:13 GMT  
		Size: 9.6 KB (9562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c045c92bb9dda3f051e0cf019189f25783553563ce873cfa4ce3ab1e324fe84`  
		Last Modified: Thu, 23 May 2024 00:00:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9a31534b3262c7b672546d3bdc4558541b955d4708b8de6f9aec7d8d048edb`  
		Last Modified: Thu, 23 May 2024 00:00:14 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef80cdf4e9322a4b00c741b8aec35f22cbd1203485b03e757db00886a53086b`  
		Last Modified: Thu, 23 May 2024 00:00:14 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685b6fc1c2d1699467b1e7d2ed40c3b5d7d6cfe742597f41119bdec270d0be49`  
		Last Modified: Thu, 23 May 2024 00:00:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:5af0aecefa6de83b92ced3d779867872dea8395fbd7fc4069f0491a8a0c69715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.9 KB (617906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35cd2e30dd131d14c04242c5f8915c6f71e695bda6bb29c7df57c1da03fd68da`

```dockerfile
```

-	Layers:
	-	`sha256:5890c27d488c8287e580c9c0ee53699686c17e9ea10bb84a1c813dee3a5e8a24`  
		Last Modified: Thu, 23 May 2024 00:00:12 GMT  
		Size: 579.6 KB (579588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772dfa1288792a958e82fa8ac899d0049efa085755e0a08d6d184f42007851c5`  
		Last Modified: Thu, 23 May 2024 00:00:13 GMT  
		Size: 38.3 KB (38318 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:5eb2698ee6a3331df0788e1786145dc248e9a33e98dd161c4d1168a9fdf12a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.4 MB (100410390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0d96fa124b8d27e9a5b4021a075f2e17d45bb1c19dcdf5a364036acecec022`
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
ENV PG_MAJOR=16
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_VERSION=16.3
# Wed, 22 May 2024 20:39:44 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Wed, 22 May 2024 20:39:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 22 May 2024 20:39:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:c2ffc53f11cd43e899fbe841af64a29fc130e402e1753b07d530dac775a0195f`  
		Last Modified: Thu, 23 May 2024 00:41:51 GMT  
		Size: 96.8 MB (96823977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c830ec00e92145d9dcd90369b41b1f2c0019bcc8282b66711a214d1e46e5de22`  
		Last Modified: Thu, 23 May 2024 00:41:49 GMT  
		Size: 9.6 KB (9568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a88ee8f418e5040a5ab3259a197bc4132deb005381a4e7c1692a29db87ab426`  
		Last Modified: Thu, 23 May 2024 00:41:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247c9fe4f7434a073b2423c52ec5a83f5c3fdebbbdc5102eac85fd75b27cb448`  
		Last Modified: Thu, 23 May 2024 00:41:50 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b38832a84df4e152d360fb79015032dca7973a0c73d22cd2e082294eab8596`  
		Last Modified: Thu, 23 May 2024 00:41:50 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b55f9d91e36d173a2ea501286a91adc42ccb5419dc27660c6575c402b2ec2b`  
		Last Modified: Thu, 23 May 2024 00:41:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:7469966f89d485290fbffd128c165710b2525cfdee68988bfb2a6b1de9d3d760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.6 KB (614625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7074cab9f02484ebe4c453d76f9dae9215cd0b1ee1c7d3ffcf1d77eda237fb7`

```dockerfile
```

-	Layers:
	-	`sha256:264652240d1f0a94583007e7f5d87be232bccfedfe7513acfd0f7b98a328237f`  
		Last Modified: Thu, 23 May 2024 00:41:49 GMT  
		Size: 576.2 KB (576194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a62c7d15a51acb4d725e546dee3de42dcec47a4683a38588d8f2a65707649214`  
		Last Modified: Thu, 23 May 2024 00:41:48 GMT  
		Size: 38.4 KB (38431 bytes)  
		MIME: application/vnd.in-toto+json
