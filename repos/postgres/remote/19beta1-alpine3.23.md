## `postgres:19beta1-alpine3.23`

```console
$ docker pull postgres@sha256:321e5a75bace9ae25ba32f0980d8b1006fe087443e35daa71947379135fdb3d4
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

### `postgres:19beta1-alpine3.23` - linux; amd64

```console
$ docker pull postgres@sha256:11526d2ff814a11aa1dd26120d3ff1a49fadf1ed6feada8f1f4a9f40a53ee1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120768886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3601ce61d1a947c781e790bddf7cb34352193aa5b8a08055b51cdf84daa9f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:50:00 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 19:50:03 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 19:50:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 19:50:03 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 19:50:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 19:50:03 GMT
ENV PG_MAJOR=19
# Mon, 22 Jun 2026 19:50:03 GMT
ENV PG_VERSION=19beta1
# Mon, 22 Jun 2026 19:50:03 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Mon, 22 Jun 2026 19:50:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 19:52:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 19:52:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 19:52:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 19:52:23 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Mon, 22 Jun 2026 19:52:23 GMT
VOLUME [/var/lib/postgresql]
# Mon, 22 Jun 2026 19:52:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:52:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 19:52:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:52:23 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 19:52:23 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 19:52:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df543903f6799c951d6696c5822b437a501471ca2b49af0dbb5197ea6f98dfe`  
		Last Modified: Mon, 22 Jun 2026 19:52:39 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80110a957efc9b124ebf3288a3cb1e13527aef006e11237e8133620ace0bfef0`  
		Last Modified: Mon, 22 Jun 2026 19:52:39 GMT  
		Size: 900.3 KB (900270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c0c5589eb0481350b429828fa2b03beb852a32c79c44ec9df5976f0306e74d`  
		Last Modified: Mon, 22 Jun 2026 19:52:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de95d3f4b83ad7e5529b4b6dea8a140f1795204d3b2f6d888d0d202647b7f9ef`  
		Last Modified: Mon, 22 Jun 2026 19:52:42 GMT  
		Size: 116.0 MB (115995689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fa9723e3625c7c7ef7b7a43b12c0859e6507876fc45ab27797aaefcfe9c301`  
		Last Modified: Mon, 22 Jun 2026 19:52:40 GMT  
		Size: 21.0 KB (21005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9ba4c9f342398fa65c07ae1a23ffa7da49f07b98b722a43947e212370c811a`  
		Last Modified: Mon, 22 Jun 2026 19:52:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59306bdc655bfd1f0cb49c1c1519c061a34f865e86b568464549b2890ade3235`  
		Last Modified: Mon, 22 Jun 2026 19:52:41 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41661260ec722520ce1f0d9307757c8c792f024ed171351f49c7eb1fc6551948`  
		Last Modified: Mon, 22 Jun 2026 19:52:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:8825d4e086d6d44f07911a72e206688af86c32a6bc0f43be699bdff19e3e7cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.3 KB (655290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234872715a81a736a47893685a4631a22318af27c91b3e126471d1d0e522671b`

```dockerfile
```

-	Layers:
	-	`sha256:24cad30e1c6537a3d8c0d83943ff68562a1104c0d669d6a8b717774db6fe6000`  
		Last Modified: Mon, 22 Jun 2026 19:52:39 GMT  
		Size: 615.8 KB (615768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44b5560c9bd13aa5cf87e62d54c4b16c27aeee3f977fee3c22093555bb833ad1`  
		Last Modified: Mon, 22 Jun 2026 19:52:39 GMT  
		Size: 39.5 KB (39522 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.23` - linux; arm variant v6

```console
$ docker pull postgres@sha256:063882c4a991ad03ea866c9c0ede27762b175ab027a29ae8b1e22e0cd7a2c4a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116970295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0096355cfedf3d4960fc5d54f73e764cb89ccd4634bda476efc89c4f2cdbe24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:49:42 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 19:49:45 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 19:49:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 19:49:45 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 19:49:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 19:49:45 GMT
ENV PG_MAJOR=19
# Mon, 22 Jun 2026 19:49:45 GMT
ENV PG_VERSION=19beta1
# Mon, 22 Jun 2026 19:49:45 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Mon, 22 Jun 2026 19:49:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 19:54:33 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 19:54:33 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 19:54:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 19:54:33 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Mon, 22 Jun 2026 19:54:33 GMT
VOLUME [/var/lib/postgresql]
# Mon, 22 Jun 2026 19:54:33 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:54:33 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 19:54:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:54:33 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 19:54:33 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 19:54:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336bc7e2b51760960136e510f865a4b5da4b4ed210d3cf64282ef1f4673c06d2`  
		Last Modified: Mon, 22 Jun 2026 19:54:46 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcd0ef97b49cbfeeea8e87f23e99864ee60890db16ebae73843e889ffa22eb3`  
		Last Modified: Mon, 22 Jun 2026 19:54:46 GMT  
		Size: 864.6 KB (864627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d218ace884864f4f7a79fc0be60a9a003e04c0c3bd68857da687dd3c1cba0452`  
		Last Modified: Mon, 22 Jun 2026 19:54:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec06e7206150e486676498b96ec69eafdcac427a0be37d5d16b08f9e40051ffd`  
		Last Modified: Mon, 22 Jun 2026 19:54:49 GMT  
		Size: 112.5 MB (112524573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822cc9daf1900c6a850ca3485b5deb3a7008a13839a8be09eceae111974d9ba5`  
		Last Modified: Mon, 22 Jun 2026 19:54:47 GMT  
		Size: 21.0 KB (21005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03213c3c110d67ddc41653eb21791d4aa750570af0c10f6e04af4d8bbe567c40`  
		Last Modified: Mon, 22 Jun 2026 19:54:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd4d2b1f500ede97280270cee15b07d625d6c25fc271d710bc4ae732fe3499c`  
		Last Modified: Mon, 22 Jun 2026 19:54:48 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844c52feec3274a844d2aee1a773555fc890994fa8853fa6287a35644a099417`  
		Last Modified: Mon, 22 Jun 2026 19:54:49 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:ed2bacb8ff8e3b6641e7af296a1fed272e347dd400dded8af85a207054cfae93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 KB (39439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a4e482940a3c8cf0871bd52d9ee0f82d8d17b375f62cfb82ee9cabee5ad2af`

```dockerfile
```

-	Layers:
	-	`sha256:45dec724d6cd8e0c53e53d31f0a7761f1521ba5c4bb8f23194e5cd6894f35d2b`  
		Last Modified: Mon, 22 Jun 2026 19:54:46 GMT  
		Size: 39.4 KB (39439 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.23` - linux; arm variant v7

```console
$ docker pull postgres@sha256:d872e7d0419b670606ad4cf21d1ecc3bc66f693db6e9c75d2b02d5e35ca61454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110503284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18911bba00321f3f095eb9b3cdcac331e909be27e2adc3e639b82861f7ae5c4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:03:29 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 20:03:32 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 20:03:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 20:03:32 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 20:03:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 20:03:32 GMT
ENV PG_MAJOR=19
# Mon, 22 Jun 2026 20:03:32 GMT
ENV PG_VERSION=19beta1
# Mon, 22 Jun 2026 20:03:32 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Mon, 22 Jun 2026 20:03:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 20:06:21 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 20:06:21 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 20:06:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 20:06:22 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Mon, 22 Jun 2026 20:06:22 GMT
VOLUME [/var/lib/postgresql]
# Mon, 22 Jun 2026 20:06:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:06:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 20:06:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:06:22 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 20:06:22 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 20:06:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ebc0a72154323991549df6941310d82e07ac04c952fd22de9a8de4ffa4e1b5`  
		Last Modified: Mon, 22 Jun 2026 20:06:35 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5539abe0fbba2eda3a42221920627fe2a5b0974fb742099e62e61ad22ee5c174`  
		Last Modified: Mon, 22 Jun 2026 20:06:36 GMT  
		Size: 864.6 KB (864631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b82110b5cd160fad263141b22abd58be617c7294effb671a71a7cd8a122415d`  
		Last Modified: Mon, 22 Jun 2026 20:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac6959642f052bd361ceabfd9d1ad96efcb1cf0468cdc87b4c2a0146965ab5a`  
		Last Modified: Mon, 22 Jun 2026 20:06:39 GMT  
		Size: 106.3 MB (106348294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101c76ae9dc3a59e49769432e5264c1da20d9521d2516bccde08b36e70bad2cc`  
		Last Modified: Mon, 22 Jun 2026 20:06:37 GMT  
		Size: 21.0 KB (21006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdc8093bf73192d4e4d55b3e5fa465ba813e092db296dcfe9876090fe914660`  
		Last Modified: Mon, 22 Jun 2026 20:06:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ae1930d500101478c566682ad369c21e9bf1899e1f84d930c67bba09f137e8`  
		Last Modified: Mon, 22 Jun 2026 20:06:37 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f10eb367899a040a85337a0e2682792d554dfa0b49c5e7530254c34bd1e05`  
		Last Modified: Mon, 22 Jun 2026 20:06:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:4cb0dde7b78b781c2dd61bb9e6822c97568f0d88b01a5ff086de9b0938b4b2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.8 KB (654786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed2285634e46a115203b5f8ec13e7e9f0310f5e73fee23b42af2ee98da6421c`

```dockerfile
```

-	Layers:
	-	`sha256:750f8bbae663f38877a44d89d43c87f5b974920668477e1b306a62103234c0bd`  
		Last Modified: Mon, 22 Jun 2026 20:06:35 GMT  
		Size: 615.1 KB (615130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d0da107ce4747327b1b3405cee15420f8317ac673578d4b326f0634ac199f27`  
		Last Modified: Mon, 22 Jun 2026 20:06:35 GMT  
		Size: 39.7 KB (39656 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:648d816991a92b37f9cfdc5c7307d2de88e2dc14c63a9afdc0634b09578b44fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118538168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be90400a38816461cdd58bc79186ff832129e496e6972b2eae8609ec654b179f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:51:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 19:51:04 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 19:51:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 19:51:04 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 19:51:04 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 19:51:04 GMT
ENV PG_MAJOR=19
# Mon, 22 Jun 2026 19:51:04 GMT
ENV PG_VERSION=19beta1
# Mon, 22 Jun 2026 19:51:04 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Mon, 22 Jun 2026 19:51:04 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 19:53:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 19:53:28 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 19:53:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 19:53:28 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Mon, 22 Jun 2026 19:53:28 GMT
VOLUME [/var/lib/postgresql]
# Mon, 22 Jun 2026 19:53:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:53:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 19:53:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:53:29 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 19:53:29 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 19:53:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b8ceafb00424438b3b353fdfcd882e1a637103410a57124e9b6da3549aca70`  
		Last Modified: Mon, 22 Jun 2026 19:53:44 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f67d0b22252cd43487ebabdabae7a8b890f7c65942786ab56be05d62ebf420`  
		Last Modified: Mon, 22 Jun 2026 19:53:44 GMT  
		Size: 852.3 KB (852282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f5c13cd9758a17e40880c26e314cc989f5e9e57ba0684955df5137f17f2be3`  
		Last Modified: Mon, 22 Jun 2026 19:53:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bac80800b92a2454242470aca936c2a895ff78ab8f036f840ce5fbafd248e0e`  
		Last Modified: Mon, 22 Jun 2026 19:53:47 GMT  
		Size: 113.5 MB (113475531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42edd6bb9c96c9d1395e3a9161f70c8c7a32afd6b7831275b7755db1541c42ba`  
		Last Modified: Mon, 22 Jun 2026 19:53:45 GMT  
		Size: 21.0 KB (21005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297a8053d95ed53d99fe881504acf41e7885c307b53bb1c73f70e36ffdd3194b`  
		Last Modified: Mon, 22 Jun 2026 19:53:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c378646198ee0855a69f57f4216ca2a0506dbd13d3407c9206c4ecdf11554e63`  
		Last Modified: Mon, 22 Jun 2026 19:53:46 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bccbd04103aaaf6c3b8d0d92fa5f7cf2186154ec3022f2147c32fadd68ded5`  
		Last Modified: Mon, 22 Jun 2026 19:53:47 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:954495ac6a04c5e31913256e8cd25ae708c2f280a6ff9e161a4853f7dc4c21a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.8 KB (654818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bd171ab70c01f17d2c1f489a86dc06a6bccc891701661f13a4e3d0607f0d26`

```dockerfile
```

-	Layers:
	-	`sha256:c8db08bdda62c1780d5d4996b7d98208cddbde056d5d3a56a058dfc24cf90a42`  
		Last Modified: Mon, 22 Jun 2026 19:53:44 GMT  
		Size: 615.1 KB (615138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c02f9fdd69a9d68a5041db14abb9fa06f9dc3628141ef3027bd30fab2bc9fa20`  
		Last Modified: Mon, 22 Jun 2026 19:53:44 GMT  
		Size: 39.7 KB (39680 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.23` - linux; 386

```console
$ docker pull postgres@sha256:a7dfff877e8353cebc3016c2d1b5d4952cb058637cbfca34c84c201ce397a598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127691874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32f23973bd37ffb4b685ecc0172d1dd962a053e288c44c2d39123c5951147f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:50:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 19:50:16 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 19:50:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 19:50:16 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 19:50:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 19:50:16 GMT
ENV PG_MAJOR=19
# Mon, 22 Jun 2026 19:50:16 GMT
ENV PG_VERSION=19beta1
# Mon, 22 Jun 2026 19:50:16 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Mon, 22 Jun 2026 19:50:16 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 19:53:33 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 19:53:33 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 19:53:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 19:53:33 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Mon, 22 Jun 2026 19:53:33 GMT
VOLUME [/var/lib/postgresql]
# Mon, 22 Jun 2026 19:53:33 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 19:53:34 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 19:53:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 19:53:34 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 19:53:34 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 19:53:34 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712b7d08f1084af685fca70662d1ef36ae72a413b0fd0f5a5b6e366da835d628`  
		Last Modified: Mon, 22 Jun 2026 19:53:51 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3958071ea0866132d6e1e6394fd1f63d577259e7c055b2659859444b03ee6738`  
		Last Modified: Mon, 22 Jun 2026 19:53:51 GMT  
		Size: 868.5 KB (868453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d192c184925b0f8770daf881157da2c9847a9e2b4d1343325bc2c9e5624a89`  
		Last Modified: Mon, 22 Jun 2026 19:53:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e0dcd95bada3f72a8980df34303727dd05e25ff4fe919f134ba56da2d12448`  
		Last Modified: Mon, 22 Jun 2026 19:53:54 GMT  
		Size: 123.1 MB (123126933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c687a60c2d5503d9ea972ee7485afcb20e7e82d727088917c3baae630df43c`  
		Last Modified: Mon, 22 Jun 2026 19:53:52 GMT  
		Size: 21.0 KB (21005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6755c35cda4ae1575112facc36d77eca6f8e397cd055860fdd0775b8b14b2c`  
		Last Modified: Mon, 22 Jun 2026 19:53:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bcbbd37b89d98de138354507100edc5007f50145f2c8a39c4325652a96fe03`  
		Last Modified: Mon, 22 Jun 2026 19:53:53 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64972cd58d8f44083511e8d74fef158b0959c7d1a3dbc36f31b2fead601af9a`  
		Last Modified: Mon, 22 Jun 2026 19:53:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:6f32153eee071a0e7d1450278e6d846db6b8ea645a9adefa1f64ba3f9be90b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.3 KB (655251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454c50fc8473b71d2dbf1cfb7b889d25c6ce67a8b6048c0239375428a829e8bd`

```dockerfile
```

-	Layers:
	-	`sha256:f6d9923528f7869f6aad328c46f2592b08122eb78071012ac678d5e3d9725dee`  
		Last Modified: Mon, 22 Jun 2026 19:53:51 GMT  
		Size: 615.8 KB (615758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6260e12ba61a6317806a5c2a6872c5cab4ffcac1855b1353adb315149fea027b`  
		Last Modified: Mon, 22 Jun 2026 19:53:51 GMT  
		Size: 39.5 KB (39493 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.23` - linux; ppc64le

```console
$ docker pull postgres@sha256:4d344f3117a36cded77da03a2e35173a1506582e128295a12610a91daed7b297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123801971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03db49fdc4127690beb2f8eb9bf9014a6725327c6fd4c3ea02b5df31c6edd821`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:30:50 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 20:30:54 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 20:30:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 20:30:54 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 20:30:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 20:30:54 GMT
ENV PG_MAJOR=19
# Mon, 22 Jun 2026 20:30:54 GMT
ENV PG_VERSION=19beta1
# Mon, 22 Jun 2026 20:30:54 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Mon, 22 Jun 2026 20:30:54 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 20:35:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 20:35:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 20:35:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 20:35:09 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Mon, 22 Jun 2026 20:35:09 GMT
VOLUME [/var/lib/postgresql]
# Mon, 22 Jun 2026 20:35:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:35:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 20:35:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:35:10 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 20:35:10 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 20:35:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e9391c05f944b123f5876a64f7d6915dbe05ee717e4f8f20d4c90a5650ddc2`  
		Last Modified: Mon, 22 Jun 2026 20:35:46 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9021869c82cf45db60d7f76a103a86eaa728469afacae3a8f0f41b2c0cf875ae`  
		Last Modified: Mon, 22 Jun 2026 20:35:47 GMT  
		Size: 857.5 KB (857475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e19e3f2b0ba329e63615d8f07287f19cf9e9c0236b3203ea893cb123230a09`  
		Last Modified: Mon, 22 Jun 2026 20:35:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70ac4862fc47bf546f0d21bc7601f979f87b62c21b88d8ba74427c3218cb770`  
		Last Modified: Mon, 22 Jun 2026 20:35:50 GMT  
		Size: 119.1 MB (119103692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9752b1a319ebcf027ef7a0c9c5c44986f1278efd75d2011c9367945a9b21453d`  
		Last Modified: Mon, 22 Jun 2026 20:35:48 GMT  
		Size: 21.0 KB (21010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f20e9b6d0d01b79941faf06e6759837cfadff7452a596f5bba0734593c1cf0`  
		Last Modified: Mon, 22 Jun 2026 20:35:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be42a901ca53276646d15a05c09827e44c55d79b2ddd745892e4e892eccd472`  
		Last Modified: Mon, 22 Jun 2026 20:35:48 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a1a365d405241ea6689200c6d9939d4c31c9278114506623c05f95ae1608a9`  
		Last Modified: Mon, 22 Jun 2026 20:35:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:e6b82f507fe3f0cf30bf290418ef27344fe983398f91806e742f1927ac892f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.0 KB (653031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3bb4270cfb33ff8fbfc4902a08df25b27da0524254b67dfaa9ee1cef5549cd`

```dockerfile
```

-	Layers:
	-	`sha256:20b9c8a1a926e60844fd335c27df018e6295d3f8f02f108e496db4851454c7b8`  
		Last Modified: Mon, 22 Jun 2026 20:35:47 GMT  
		Size: 613.5 KB (613471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e8d492d2cc99cdbdd0ccad19399db8b0766be6acb68b59dc3022cb8ca2bfa8`  
		Last Modified: Mon, 22 Jun 2026 20:35:46 GMT  
		Size: 39.6 KB (39560 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.23` - linux; riscv64

```console
$ docker pull postgres@sha256:e60d655f46421f0db01eac140cd0e61e069e5150d37ae747f060c8b3d26f1c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125610900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea631d86e250b349bbb5c04b1751e04b9620f6a9ef0c5ae387738d49fedb6d2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 17 Jun 2026 21:19:07 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 17 Jun 2026 21:19:18 GMT
ENV GOSU_VERSION=1.19
# Wed, 17 Jun 2026 21:19:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 17 Jun 2026 21:19:18 GMT
ENV LANG=en_US.utf8
# Wed, 17 Jun 2026 21:19:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 17 Jun 2026 21:19:19 GMT
ENV PG_MAJOR=19
# Wed, 17 Jun 2026 21:19:19 GMT
ENV PG_VERSION=19beta1
# Wed, 17 Jun 2026 21:19:19 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Wed, 17 Jun 2026 21:19:19 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Wed, 17 Jun 2026 22:12:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 17 Jun 2026 22:12:22 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 17 Jun 2026 22:12:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 17 Jun 2026 22:12:23 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Wed, 17 Jun 2026 22:12:23 GMT
VOLUME [/var/lib/postgresql]
# Wed, 17 Jun 2026 22:12:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 17 Jun 2026 22:12:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 17 Jun 2026 22:12:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2026 22:12:23 GMT
STOPSIGNAL SIGINT
# Wed, 17 Jun 2026 22:12:23 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 17 Jun 2026 22:12:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65f72f9dc4191057d4290d81d3e9b85a1e898cd4566300956d6f215da3e5d2b`  
		Last Modified: Wed, 17 Jun 2026 22:15:32 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfbfbc6e54c945a01fa3a875eb6f9cecc112c80d1bfc687accbcd8cac7b9050`  
		Last Modified: Wed, 17 Jun 2026 22:15:31 GMT  
		Size: 867.5 KB (867539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab6f95812a5a3ce33b21e4c648495817997b01d0e1c0e1bd07538f3f721ede0`  
		Last Modified: Wed, 17 Jun 2026 22:15:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb368270e488d34699e28d6196c4ca565ef34c3a50e83acef91f397bbccc7a5`  
		Last Modified: Wed, 17 Jun 2026 22:15:50 GMT  
		Size: 121.1 MB (121127187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8d77506a48b83fe13c0e52096614f7c5d702505dd3c7a528b804a5d93cec8d`  
		Last Modified: Wed, 17 Jun 2026 22:15:33 GMT  
		Size: 21.0 KB (21013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5dfdcae3be73278b4bb990be3fced40eadbe4ac51111438261af1f699f6196`  
		Last Modified: Wed, 17 Jun 2026 22:15:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d46003ed1b7462c57c29482454d3795a001ae8f87488ef90ad6c8503808c4a9`  
		Last Modified: Wed, 17 Jun 2026 22:15:33 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dc8e4abc9e173b3ef96c56d8de1338111bc0899b51b3f44aad6fa02255d241`  
		Last Modified: Wed, 17 Jun 2026 22:15:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:b1c7a22d1b20ed885410cc90a3b64565f794a5164dd1a56a247eda4c9f9b0a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.7 KB (654689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7039d85e29854ec0c1ec8832f9c6feff37eef50dd4387178fdeb4df7727eeba9`

```dockerfile
```

-	Layers:
	-	`sha256:ddf3900c30235f8db7fc6f939c90ebcd393be85391e0315758213acc4d4234b8`  
		Last Modified: Wed, 17 Jun 2026 22:15:32 GMT  
		Size: 615.1 KB (615129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dec490e2eb7716b108a7aac85584e628fa64a75a1f1328f95fa3ebe255dc698`  
		Last Modified: Wed, 17 Jun 2026 22:15:31 GMT  
		Size: 39.6 KB (39560 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.23` - linux; s390x

```console
$ docker pull postgres@sha256:90d79866e7798996efb5de3c85556848078a29c31b1ebaa23ebe0c6c9414456d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127332381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58927ecead46046003e610218fa01cf6b458003307aef6c3f128ea772783b02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:02:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 22 Jun 2026 20:02:17 GMT
ENV GOSU_VERSION=1.19
# Mon, 22 Jun 2026 20:02:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jun 2026 20:02:17 GMT
ENV LANG=en_US.utf8
# Mon, 22 Jun 2026 20:02:18 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jun 2026 20:02:18 GMT
ENV PG_MAJOR=19
# Mon, 22 Jun 2026 20:02:18 GMT
ENV PG_VERSION=19beta1
# Mon, 22 Jun 2026 20:02:18 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Mon, 22 Jun 2026 20:02:18 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Mon, 22 Jun 2026 20:05:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 22 Jun 2026 20:05:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 22 Jun 2026 20:05:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 22 Jun 2026 20:05:52 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Mon, 22 Jun 2026 20:05:52 GMT
VOLUME [/var/lib/postgresql]
# Mon, 22 Jun 2026 20:05:53 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 22 Jun 2026 20:05:53 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 22 Jun 2026 20:05:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jun 2026 20:05:53 GMT
STOPSIGNAL SIGINT
# Mon, 22 Jun 2026 20:05:53 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 22 Jun 2026 20:05:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dcf63c964792512f3f7a826a74a49054cebe7cc1e0ac6e05fa7396806c67cd`  
		Last Modified: Mon, 22 Jun 2026 20:06:19 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfed1bf23e7b1309208c3b686d6f6dc526033533f2b7dbe99ca30e87d28e6bd`  
		Last Modified: Mon, 22 Jun 2026 20:06:19 GMT  
		Size: 874.5 KB (874495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d4612681e2cde1caeef7867176188ebdf5d455acc2fcb15fc8b23137754e1`  
		Last Modified: Mon, 22 Jun 2026 20:06:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadbae70691d96f69b8a671eee4916ae76dc1bce3064f35e4029253d99539e33`  
		Last Modified: Mon, 22 Jun 2026 20:06:22 GMT  
		Size: 122.7 MB (122722135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d1a5a471a2c179f6fa10fe6534426a8d28b81e6d494741d62e960d391a8094`  
		Last Modified: Mon, 22 Jun 2026 20:06:20 GMT  
		Size: 21.0 KB (21003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b913ae35e0cffefbe5481396d2efd4e0797d68d126288ec3451a21fbdb0e0a`  
		Last Modified: Mon, 22 Jun 2026 20:06:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d034153911bbfe36093d43f8a1bf7c96bfd14b04f231f0a4d7ef8197535ca31e`  
		Last Modified: Mon, 22 Jun 2026 20:06:20 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd39c322ecdca299c7fb88282dafd2549478acf19bfe55f2f3d5b2cfa0a3cf5`  
		Last Modified: Mon, 22 Jun 2026 20:06:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:3e21aedb9a2ad05d78a886185ffb2cc40d0869f1cc8639d5e1da3b49e9440313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.6 KB (654639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fceacf3e39d5c9a1c29263d8493af7d092a0bbfd1071c9f234a8911b2df0f66`

```dockerfile
```

-	Layers:
	-	`sha256:ccb3b78e7150cbe731ecdcd4724c496b26893e49b9c2e75f9b63e79668001b14`  
		Last Modified: Mon, 22 Jun 2026 20:06:19 GMT  
		Size: 615.1 KB (615117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ad62e9d5ac7e444a54c26ee81091438911e50b57330f66e622c3f787dd61da0`  
		Last Modified: Mon, 22 Jun 2026 20:06:19 GMT  
		Size: 39.5 KB (39522 bytes)  
		MIME: application/vnd.in-toto+json
