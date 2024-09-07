## `postgres:17rc1-alpine3.19`

```console
$ docker pull postgres@sha256:50bef1ca920c83bdd054b5659bb8deade9582c2e220563c2919d82b545d46948
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

### `postgres:17rc1-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:25f6eebba1788467ff88f3b4b47adc11a5834adae4db6182c5e3e8a50e917c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98102106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fef6cef6f38aa1e2feffdc5586fa14bbfede7399693cba00bd5e614a167261b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 05 Sep 2024 13:44:37 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17rc1
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_SHA256=cef689e2de8c3d605d8406c065573b8d70859fc6f2a8d720b0d98a6d62ef16e8
# Thu, 05 Sep 2024 13:44:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305e4b85986f142e321dd086803bc5f6f225a5bd3e1b94f108d7bd549a493ded`  
		Last Modified: Fri, 06 Sep 2024 23:20:53 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f86375ff723fb62502440bc0ae7c5a32ac1db7fa009478e50c51be1c20fd6b2`  
		Last Modified: Fri, 06 Sep 2024 23:20:54 GMT  
		Size: 1.1 MB (1120291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c372e1c69040eaddb55de734fdfc77b5769e47bfc361246bc710ad7d5215a44d`  
		Last Modified: Fri, 06 Sep 2024 23:20:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6961b71ebfc4fd7655a41ef05e546d9a0fd868eac3450d47d918c1a84d5dd16b`  
		Last Modified: Fri, 06 Sep 2024 23:20:55 GMT  
		Size: 93.5 MB (93544947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bbae72c5667df0502140deb628a714bd33179a9f6f388e8d222a084a81f676`  
		Last Modified: Fri, 06 Sep 2024 23:20:54 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66151ef421ca9604ccb7da2266ba8132c408d61d082406796e5c164bf13e7722`  
		Last Modified: Fri, 06 Sep 2024 23:20:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebd8d7c2b9d64360dc4bb6c309df1ad46a70132982dbc0ba55ce567e8d7ec8e`  
		Last Modified: Fri, 06 Sep 2024 23:20:54 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0bb776bfa5b4cd05aaf54231db23d7db7cc84bcff14ee2f75b7e19d904f6f5`  
		Last Modified: Fri, 06 Sep 2024 23:20:55 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b61b8646b2dda5ba12ffd307aa4628646a9e7856089a5c9cc0088140f0c7507`  
		Last Modified: Fri, 06 Sep 2024 23:20:55 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:b88dde1e6ae14b760648c78c641f17bd4de978dd3bce9829f800e74610297bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819a5cd7a3d6f2db73143b543f5cd62d22599a06fc1c984e33d3510df0eed24d`

```dockerfile
```

-	Layers:
	-	`sha256:c3c8351b8844ce4a555b2dcbc197dae0a9ba996e1f52b8c84788c59775c08103`  
		Last Modified: Fri, 06 Sep 2024 23:20:54 GMT  
		Size: 968.4 KB (968369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e20483e98184e1c9147c8f0f0fa41e9c387402b7e45a4c1053170f4251028a9b`  
		Last Modified: Fri, 06 Sep 2024 23:20:54 GMT  
		Size: 42.1 KB (42084 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:8fea8b043bc5f56c25fd3a5bb1c9594f448fd64d08cc2e6ca67b7b520dab9ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96751197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a02dc300116ac42df41d559ff3862dbdc60151b6758a2ddfd30fc4220ac4de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 05 Sep 2024 13:44:37 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17rc1
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_SHA256=cef689e2de8c3d605d8406c065573b8d70859fc6f2a8d720b0d98a6d62ef16e8
# Thu, 05 Sep 2024 13:44:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d826e605346ac703fd4bb49c66f0da21ade0330bd6f0365a01ffacb9e9b5bd`  
		Last Modified: Sat, 07 Sep 2024 08:48:26 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65abd2f8c8203e91dbd2e59181770a8eee351135174c82c7167d10017bd7f7c6`  
		Last Modified: Sat, 07 Sep 2024 08:48:27 GMT  
		Size: 1.1 MB (1086689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40167ca09e520a497007dcfa6eb16e9b748aadaf5604c9068b72b2c41196b05c`  
		Last Modified: Sat, 07 Sep 2024 08:48:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2153f0ea12a9613b977f15dfadfea6cd04fba0ff1496d6836dd10dd8f51e5587`  
		Last Modified: Sat, 07 Sep 2024 08:48:30 GMT  
		Size: 92.5 MB (92470950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0222f73ec675f4deab348bfcbc0e856ab31f9647e8826c3a0a12c91874f47c1d`  
		Last Modified: Sat, 07 Sep 2024 08:48:27 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732b13057bc4cce8d5b0400c0f291d9720f1f69c414bb62fba061e6ab9177ba6`  
		Last Modified: Sat, 07 Sep 2024 08:48:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9695045b8f32b2e7e047bec893e35fe4ea8f593cb01f1de3d39fb9ba22eb2f`  
		Last Modified: Sat, 07 Sep 2024 08:48:28 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befe3a931e1184e14c17a12d115370850723ff86a9652dcc96ffb10ac05f3027`  
		Last Modified: Sat, 07 Sep 2024 08:48:28 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f574ec9087e1343a3e63d252697bd64d276a46bcca66d0d11d6cc1ebf546f58`  
		Last Modified: Sat, 07 Sep 2024 08:48:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:30a3caf7f815c7a47afe5c80ba500eea5aa4a77fd5bc8d59f8242dfbd6a11390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 KB (42001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97db5645ebac14ec09f0bab1a6de5948f598cf2a847f499097d51e2536c58894`

```dockerfile
```

-	Layers:
	-	`sha256:413d9a4a958c0e2507b4e4a362760332cd3dd284980dc9f78b51f513ab0d77fb`  
		Last Modified: Sat, 07 Sep 2024 08:48:27 GMT  
		Size: 42.0 KB (42001 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b574d7d68e529797e21623592b7dbfd9d8716dd8da562e4ad9e43a71c7694515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91146707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252ef997db65c9b5715d0293a67fe128c760f8503f11128b9b4bb15d9d671109`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 05 Sep 2024 13:44:37 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17rc1
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_SHA256=cef689e2de8c3d605d8406c065573b8d70859fc6f2a8d720b0d98a6d62ef16e8
# Thu, 05 Sep 2024 13:44:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7301be67e4738b26ff038817b98ba1651b096b6f4c8282ec263badac035e791`  
		Last Modified: Sat, 07 Sep 2024 09:11:15 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f6bf8db32a8805b9bb6360898111fe2af1e0d20467f3823409618a0fc832e6`  
		Last Modified: Sat, 07 Sep 2024 09:11:16 GMT  
		Size: 1.1 MB (1086692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43c79d41c60cf8f8fa38fbe19658b61e9d619a905bfb5e78b7e56bd4c73950b`  
		Last Modified: Sat, 07 Sep 2024 09:11:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18dc0f7906e6720ebe56a6813ef2bcd862b1b64ec2c2fc20a0943a44120a62d`  
		Last Modified: Sat, 07 Sep 2024 09:11:18 GMT  
		Size: 87.1 MB (87115180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bafff572dc878a692ae7436763db4e869cd5ddb41f30a040fb65163e9c829db`  
		Last Modified: Sat, 07 Sep 2024 09:11:16 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b1d7962e8f8e30b615132b63e53355d24dbe5373b3106974e5a26816272263`  
		Last Modified: Sat, 07 Sep 2024 09:11:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d438287f89f478d91f6e4fa171304aa3d654b3232b1440356116230bdfbb5e4c`  
		Last Modified: Sat, 07 Sep 2024 09:11:17 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3a3c1037a1178e070782665f0a4869de2f144d5406be419832ba29f6698276`  
		Last Modified: Sat, 07 Sep 2024 09:11:17 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca5827ef91ac2e57e24e1ef5197489a3af3c6d602d473108dbbd70181b11171`  
		Last Modified: Sat, 07 Sep 2024 09:11:17 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:0f874a90e6304a802835a600b0dd2b4726f8f7ccc8dd45ed1d34f9a2e8e2fdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaa3087af7ca5bbae5d8a6e11db8a955e3e0cca3581fa775e1f90793bc389e8`

```dockerfile
```

-	Layers:
	-	`sha256:2d9bf2ed500b0b5f3abd156edc268d8e2e31d2c9154fd3098322a81c15e6a1cc`  
		Last Modified: Sat, 07 Sep 2024 09:11:16 GMT  
		Size: 968.4 KB (968381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4f6c55e82feadf73778a078a1af5bb61af140d99fc20c1518db861942a1d26e`  
		Last Modified: Sat, 07 Sep 2024 09:11:15 GMT  
		Size: 42.2 KB (42221 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:35e80bcd16d7298febe0f5a7aa8ff3030a67d12b03e9e2924d4b5289c443ad78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96760510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0159b6a4f4fdca1dd09f980b93e92721a7ddd4b7ddbf09547a7764dd104c80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 05 Sep 2024 13:44:37 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17rc1
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_SHA256=cef689e2de8c3d605d8406c065573b8d70859fc6f2a8d720b0d98a6d62ef16e8
# Thu, 05 Sep 2024 13:44:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896d03877eb37d824efa1dcb1e0aa39cdef05d3080317292a8ddd2075f6fb7a3`  
		Last Modified: Sat, 07 Sep 2024 08:46:55 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb628377f51a21b951e4859e56c887983ad44edd0c0d40e10a1a4781b8f6ce7`  
		Last Modified: Sat, 07 Sep 2024 08:46:56 GMT  
		Size: 1.0 MB (1049350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69206b2afe7893df32fb102385cf23de31844f1fc715877dc68f2a043765569c`  
		Last Modified: Sat, 07 Sep 2024 08:46:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc3c152381e1bd03f390f86920d92b68de9a5f2292650b57d3fb7f64f3544a3`  
		Last Modified: Sat, 07 Sep 2024 08:46:58 GMT  
		Size: 92.3 MB (92334893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc83305a9346695168e23efa155df4908f7695c27526d427ce3c65b39fab2b7`  
		Last Modified: Sat, 07 Sep 2024 08:46:56 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd33c3b6465063e4c129212ad7c3afcf3340a153624c80f10559e1cfdea55ac9`  
		Last Modified: Sat, 07 Sep 2024 08:46:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e539bf0cf824caed4c2a2db5640fd2cc84a1547950800e5e508cc62b5d9b45a`  
		Last Modified: Sat, 07 Sep 2024 08:46:57 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f528fab2a5fb7ca437054291a54fdc2b89ed6eb693e9b018225b2c512ee7158c`  
		Last Modified: Sat, 07 Sep 2024 08:46:57 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38133016b4c6410cb5e91d199bb37284a1d1d3ffa2d5fd27eb2b5c7a1ad93903`  
		Last Modified: Sat, 07 Sep 2024 08:46:57 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:4aeca0b735cfdb8b957c84bebc038df76d086c137bca93cd7de533da431e43e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8838322b880e9880d6d71c70255d2e9cfef1518112e8fd5676f8c23bcde23350`

```dockerfile
```

-	Layers:
	-	`sha256:99c8ebe49666ce73977106e2363a02f64b7164730be52f5e95941bbc12ee8a2f`  
		Last Modified: Sat, 07 Sep 2024 08:46:56 GMT  
		Size: 968.4 KB (968389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dedb3d95c4f5c1edb746fac1ca604884d70390abc06205a4ad542fcd9ddbb06`  
		Last Modified: Sat, 07 Sep 2024 08:46:55 GMT  
		Size: 42.3 KB (42348 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:5810608c9066b10bce19ecb133d6d220508776cc2d4025bd99c2b4fbf81d0acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103399991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7ccb899bb88d6e19f3d0671954792d5227641d799ce63783d32d632db9c227`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 05 Sep 2024 13:44:37 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17rc1
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_SHA256=cef689e2de8c3d605d8406c065573b8d70859fc6f2a8d720b0d98a6d62ef16e8
# Thu, 05 Sep 2024 13:44:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98373a76c77952cdacae71ca9eb554149a917635f3c0277e89908a4bf3a4135b`  
		Last Modified: Fri, 06 Sep 2024 23:21:07 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baeee3d561a93bb48c00fe79ffb94f9e6e4eb9fada1d74d97cd21c8c445e643b`  
		Last Modified: Fri, 06 Sep 2024 23:21:42 GMT  
		Size: 1.1 MB (1095477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40010d638e863e0cfed47de3489efbc5701882ef9ec6712538c88af544b9b1e3`  
		Last Modified: Fri, 06 Sep 2024 23:21:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb653093076092f0ff58d21721ee2a0ccf75114a653e3699a1262d263a08b85`  
		Last Modified: Fri, 06 Sep 2024 23:21:48 GMT  
		Size: 99.0 MB (99033745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61f3492f9d3d9811a27efccea93d256719fa05fbc66fbac24a08bf0a062b54d`  
		Last Modified: Fri, 06 Sep 2024 23:21:42 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a377a913f665d22b29fc430f0a7369114c5b8775c22eb1dcb5d26bee9441b4f6`  
		Last Modified: Fri, 06 Sep 2024 23:21:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e407975b7b0506951ddeeee65ce830c1ce882c30c904c9cbdad4a8805423a3ee`  
		Last Modified: Fri, 06 Sep 2024 23:21:47 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea91a9329bd660b6aa74bf552d0b27c5c69ba16424ed2b7b90c86b57158d457`  
		Last Modified: Fri, 06 Sep 2024 23:21:43 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7790b3a6e8bcf6fb97ef817ea2f1e70cb46c4e0e459eb92b4a0d655dfb1e024f`  
		Last Modified: Fri, 06 Sep 2024 23:21:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:b89d5c725d485f7ccc6c0a060e405af6c3550faee89498024c1517780ec78bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e8f9f6792ef995530c15cfcf101c7ec59a000614d0bce00009d7e31d8d9f15`

```dockerfile
```

-	Layers:
	-	`sha256:97f3778b006f0cae852fcc303d65ede9e2284050972bdf02ac14e7f2e883d219`  
		Last Modified: Fri, 06 Sep 2024 23:21:42 GMT  
		Size: 968.4 KB (968359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:532ec333e56e8ded92281ff233db3b0661d2dbf9f02a2abbd25bb59d69e51f04`  
		Last Modified: Fri, 06 Sep 2024 23:21:42 GMT  
		Size: 42.1 KB (42056 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:01355d9261bf6454e18fbc127b61a4828498990e22441e031a7f70190a5a859c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102698650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b12f37e66f295ec88cd8cc41f00004a6f6dc1947b0192fae6a20b7a0adaf42f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 05 Sep 2024 13:44:37 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17rc1
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_SHA256=cef689e2de8c3d605d8406c065573b8d70859fc6f2a8d720b0d98a6d62ef16e8
# Thu, 05 Sep 2024 13:44:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02f5f490f95d2b3fc6f063070a7454d2c3bc3e3fbf1a39ccb5cfb232b5c54a7`  
		Last Modified: Sat, 07 Sep 2024 08:15:21 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e90f8e25b6668b7d290e0dd4df1451615699705988c9e87c111e2645e26782`  
		Last Modified: Sat, 07 Sep 2024 08:15:22 GMT  
		Size: 1.0 MB (1039691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95d72b03637bf78c26bda07ad18e6c967a30d0f45b636a23d3324c697dbdef1`  
		Last Modified: Sat, 07 Sep 2024 08:15:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cb5358760276c75dc635d8e823017a698fd69a9995fa0147ee60d14cf58b85`  
		Last Modified: Sat, 07 Sep 2024 08:15:25 GMT  
		Size: 98.3 MB (98277324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0c06c9a5f107d521c8208256da07381b6bc5433c55caec4016f5a34347d03b`  
		Last Modified: Sat, 07 Sep 2024 08:15:22 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d6c06b99bfe5e47f23bdec4c42c601d23ace3174e9175be366aba4438abc0a`  
		Last Modified: Sat, 07 Sep 2024 08:15:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35efe9447cec6f23dd39f0731a10be95a1a37b19f2437b19f7723c046d1889f1`  
		Last Modified: Sat, 07 Sep 2024 08:15:23 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e282235bef96a2b7786d9f8595272977fcbb72de3d1525bbc171cf3de75b0117`  
		Last Modified: Sat, 07 Sep 2024 08:15:23 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953494939232063ed8cfec9010a81d98be653b0ab6cf0c8d85b0e83483312864`  
		Last Modified: Sat, 07 Sep 2024 08:15:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:8e2a00c1b0e629963db627032a89e861f5ce0211defc788c2a50fd4cd73f4ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1006885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a003bbec6f20f2be4c413ff185e552315fc3c21c928f8bd841e3ccbfa1944a9e`

```dockerfile
```

-	Layers:
	-	`sha256:d3f57bb23997c4c39af84e990a4f603333d86011bef551f7678ec93d85ead505`  
		Last Modified: Sat, 07 Sep 2024 08:15:22 GMT  
		Size: 964.8 KB (964767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73a1c121ba80dfb9fc14fc5353c09cb866d74c9211c8343dd36eb9c393b0564b`  
		Last Modified: Sat, 07 Sep 2024 08:15:21 GMT  
		Size: 42.1 KB (42118 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:a35cba324887434a889c0e3c6f405b7efadcb5a503a1be26b47c2ef486a08336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 MB (106990955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b20d6cd8678d0dfb76f176e84713d34dcb4382d9c27c645398bb0cf7e1e997f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 05 Sep 2024 13:44:37 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17rc1
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_SHA256=cef689e2de8c3d605d8406c065573b8d70859fc6f2a8d720b0d98a6d62ef16e8
# Thu, 05 Sep 2024 13:44:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b332d47914fd31ead4a60b0094c348297bc38ef29f5b3eb692132ff8910b0e9a`  
		Last Modified: Sat, 07 Sep 2024 07:33:17 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a0768a2d48558dddbc4835820dc9de94b42c05a140368d161f5ac6a9ae6d49`  
		Last Modified: Sat, 07 Sep 2024 07:33:17 GMT  
		Size: 1.1 MB (1083902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24701e91ad916951f784865dcffde3a257d7a15e2ea9b7a93b4318aa9afa2d26`  
		Last Modified: Sat, 07 Sep 2024 07:33:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e6ccfdca3c9a80eee91bf703785d546123aff820ecbf3108e2f144a232fc3c`  
		Last Modified: Sat, 07 Sep 2024 07:33:19 GMT  
		Size: 102.6 MB (102636522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a3f5c4f7de017d286fd7546bfa1e5d32db684845d5de5dc9dea6c43b4ce068`  
		Last Modified: Sat, 07 Sep 2024 07:33:18 GMT  
		Size: 9.9 KB (9888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3ba8f4686c7c8cd248612e7ba0d7ae1f1a0d42cc3d310866cf9e10c60beeb1`  
		Last Modified: Sat, 07 Sep 2024 07:33:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9fdf9961dc338b6af4c13e70d9513bb90763e500c4005e8618bf30fd582f4f`  
		Last Modified: Sat, 07 Sep 2024 07:33:18 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a057c178b4d4afb264d004bff0605bcf4aeaf608c6c2889b1fdf16da668e2e5`  
		Last Modified: Sat, 07 Sep 2024 07:33:18 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346560bab92ea4d3a83842770e6f99616a2109e4c42e735c0c93975ac808318e`  
		Last Modified: Sat, 07 Sep 2024 07:33:19 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:78edc171daf5a1f4ef4ad021f8e90c277f8154d42ea560197bef616a7f09bb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1008505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9c28957710f50100a2778bf7d783d515884dff5c044207a7a3313cd397fbee`

```dockerfile
```

-	Layers:
	-	`sha256:efce8b12527d9772c0150c49c393f2f9be3735fcc0edcd6e15d40df4bb709826`  
		Last Modified: Sat, 07 Sep 2024 07:33:17 GMT  
		Size: 966.4 KB (966415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:620fb874e945e8f65d940405da75f9038db8dc102cea4705d953aab814138c2e`  
		Last Modified: Sat, 07 Sep 2024 07:33:17 GMT  
		Size: 42.1 KB (42090 bytes)  
		MIME: application/vnd.in-toto+json
