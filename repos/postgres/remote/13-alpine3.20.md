## `postgres:13-alpine3.20`

```console
$ docker pull postgres@sha256:5876360d7343b5d322a98fc9abe790e1ecbf68dde2a6f07724e164a6cc38587e
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

### `postgres:13-alpine3.20` - linux; amd64

```console
$ docker pull postgres@sha256:e672df03d60fa3c8800685800859fe1adb6f88138ae51ab242e1490701833d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96136077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd6c65c722fd870bc49ff651eb7b397331751854aaf14a67ba731973e66686b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:37:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_MAJOR=13
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_VERSION=13.16
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_SHA256=c9cbbb6129f02328204828066bb3785c00a85c8ca8fd329c2a8a53c1f5cd8865
# Thu, 08 Aug 2024 16:37:43 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:37:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:37:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5209ecba34ad72bdf3c371c2a6dee54956d6a72c43ca28f8f4841685c6a4f67`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 987.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5339c444fe1783a26e84173f5f8ccec03a59222871d3df310cdb9a8c7f3301c0`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 1.1 MB (1119776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e4fd09ad51fca1cb26f4982eb645fc878786e0c4d1412bd1d2382696df39ec`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0aade08360305d398efe27f2f6c4a67ea9f87ec790bce41802be9dcaed6d35`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791eee8f12d1a44be2edc3451f6e1e73f333727f119bfbe6cfcf5038481079ae`  
		Last Modified: Tue, 12 Nov 2024 02:39:01 GMT  
		Size: 91.4 MB (91376209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e86ab1c13adfae9a9472e53ef24ec94d37c53f7fee2871b7d187c4a8b4f6f99`  
		Last Modified: Tue, 12 Nov 2024 02:39:00 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e6549c2f4b02550ae5de5fd61f5ffaa759f45dff41c25ae0c4f85eff57a49f`  
		Last Modified: Tue, 12 Nov 2024 02:39:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039c08daefd56b758c5ea11895547a38b8da86fe82c9e630d791652c66adbe6d`  
		Last Modified: Tue, 12 Nov 2024 02:39:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddf347a64cedea8a6f7e4fcb118d1b10f970cf7dafa8eb0d0a491873111d087`  
		Last Modified: Tue, 12 Nov 2024 02:39:01 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4432ce6be0d2f3927ade57522bb7d8d500e985d93b48fffcc5b92c3b4dd769b6`  
		Last Modified: Tue, 12 Nov 2024 02:39:01 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:950cc2300eb213040313ea170782430640edeb3f365cc9b8f59f34272ec32090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.4 KB (633382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fb568308b332c11349f82b07bc03358f02d5a560f095e5becd40d1f171d0d1`

```dockerfile
```

-	Layers:
	-	`sha256:d97640ca9a00f0aa287a4da1b5bce52a2d0dd4859c8ff81bad3d73867987f9eb`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 588.1 KB (588073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:152c09ab63fdaef70967b971759bbaa66d45df4358e1fac4f03a1df6c20a0aa1`  
		Last Modified: Tue, 12 Nov 2024 02:38:59 GMT  
		Size: 45.3 KB (45309 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:29f80079db0bf07cca0dfd9f1daa9ee5cb6e5b7e6a8604180260384117751af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94607438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2060a7f7462f2bb7569fe411deb4e104eac9dbd8f9b57c38b2f164d5d285259a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:37:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_MAJOR=13
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_VERSION=13.16
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_SHA256=c9cbbb6129f02328204828066bb3785c00a85c8ca8fd329c2a8a53c1f5cd8865
# Thu, 08 Aug 2024 16:37:43 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:37:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:37:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c571936168ff49222fc45202f5453daceaaad85841344e7a56766ac0c06bcc0b`  
		Last Modified: Tue, 12 Nov 2024 05:37:05 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd27d05dad1bb8227f4e72ddcbdcd2601f74b55f8b2929cff613d173bc82672`  
		Last Modified: Tue, 12 Nov 2024 05:37:05 GMT  
		Size: 1.1 MB (1086464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68300102007bc93827d658bcc2e3930a994d78385553143780dadcc3f284915a`  
		Last Modified: Tue, 12 Nov 2024 05:45:35 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef5933ae7af9d77048b5e8ce8dc6807af55c837feaeaecb0fac68b44b61199d`  
		Last Modified: Tue, 12 Nov 2024 05:45:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fa766fcd62260f9b4fc583388df55f13de5f37e47b5c0f4e838c1f5b01d766`  
		Last Modified: Tue, 12 Nov 2024 06:09:45 GMT  
		Size: 90.1 MB (90138179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784e38f1d111cd7e06a9d094dd826eb92d09fa95556c2b684cc5597a7f567bf4`  
		Last Modified: Tue, 12 Nov 2024 06:09:42 GMT  
		Size: 9.0 KB (9021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19efc5c58335e0e80e7b7a4b2298c0380e748e8c05d3828a62e450682605ee0`  
		Last Modified: Tue, 12 Nov 2024 06:09:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05f6d74b2322c34222eef24db1797fc9d31ffd2b95aea75ce1a893fd34a7b88`  
		Last Modified: Tue, 12 Nov 2024 06:09:42 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400e7eab1298bd0ce3f416bf152f982dbc75e3c9168da56e577f208eca66faf7`  
		Last Modified: Tue, 12 Nov 2024 06:09:43 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1ef978dee77789299c45e3a5e87c36e134e6befbfb2ad39f09ca6d1431f38d`  
		Last Modified: Tue, 12 Nov 2024 06:09:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:da4bb11ed78574123dfec291fd9bddd44556628c0488c4caa1984c4a7a12dc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 KB (45275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d78866ac73cb77cfd13756746a336fae7f87a2b2d80b3f28386193e2d14c4aa`

```dockerfile
```

-	Layers:
	-	`sha256:a3dd5691dd02bbf02324841320c9a2bf06c67e20cdc4c75195a2ebea508e5b95`  
		Last Modified: Tue, 12 Nov 2024 06:09:42 GMT  
		Size: 45.3 KB (45275 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:2699325cf9bf1248ca0c266de84f2ce237f7d7e3275df5c6432ef0d6f8132690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87123185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af310790887a8e3a5f2af4d0e3ac9aba1de11da02da18cad209e2ba31ffd4ae7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:37:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_MAJOR=13
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_VERSION=13.16
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_SHA256=c9cbbb6129f02328204828066bb3785c00a85c8ca8fd329c2a8a53c1f5cd8865
# Thu, 08 Aug 2024 16:37:43 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:37:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:37:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ac8e9d0c68b096b09818bfb20f42e953c3d9cd9df375198a3b549dd5ce5f63`  
		Last Modified: Sat, 07 Sep 2024 09:07:01 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea95758d71d5413b7fd57d98797bffda5c623934cbefc0067a635c1ff9f62e9`  
		Last Modified: Sat, 07 Sep 2024 09:07:02 GMT  
		Size: 1.1 MB (1086468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f93540d99e99914202c8ed07dbb4762ba225d2c6061670c2fafc29c7af5b206`  
		Last Modified: Sat, 07 Sep 2024 09:15:08 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8913630691ba9994e15bc5ad692e83b0d35705f5db68d326926e420ae066c0e7`  
		Last Modified: Sat, 07 Sep 2024 09:15:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49091750e52c3f597b1ad13321150a549127e16ba194f16faa06a921b9f58d2f`  
		Last Modified: Sat, 07 Sep 2024 09:37:29 GMT  
		Size: 82.9 MB (82925018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2578a85604e56514ddc446247f40db0dae2ac595f0d53e074ece535ccc9e6a30`  
		Last Modified: Sat, 07 Sep 2024 09:37:27 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9531d29ddc30f7ca5744fc9f5aa94861d9890aeda5079d6ce3c26755a95ca0`  
		Last Modified: Sat, 07 Sep 2024 09:37:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49496e4db1a9720268ade908c6967e8d18d99156ac9c5e4ce335d91483df54e4`  
		Last Modified: Sat, 07 Sep 2024 09:37:27 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1015e2560fa149a48d282cd04d4ab21a087b87b2808a536a56da8be342e98828`  
		Last Modified: Sat, 07 Sep 2024 09:37:28 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0374eaa03eb6fffdbf86dba69dc3f90a9c745be20ec175c42ddbb71d65ae870`  
		Last Modified: Sat, 07 Sep 2024 09:37:28 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:e41cf41f39c1042b634e3fa4b6a68c5b8dde7202d23e09f41a03e001aca47225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.1 KB (633082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff2a5b576afcda5fa2d04d19f8552f5068d82f57f52044f7e43e1bbb48ee3b27`

```dockerfile
```

-	Layers:
	-	`sha256:26db3da563f33915c9c373785529a8c67fd3b6e17f224102cf641851d3d9eb05`  
		Last Modified: Sat, 07 Sep 2024 09:37:27 GMT  
		Size: 587.8 KB (587791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:453aadafd63cdf292988faa4174db0a671efb4c43f8652fef116c0e2ca3cdb5e`  
		Last Modified: Sat, 07 Sep 2024 09:37:27 GMT  
		Size: 45.3 KB (45291 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:540fe77de75066705cf769529f837e87f2ef7ca981ecbc5912a026a670041e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93112105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339e83a7734542bea939c705674f151e05b29c08dd0b51c1565ffa688d359d30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:37:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_MAJOR=13
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_VERSION=13.16
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_SHA256=c9cbbb6129f02328204828066bb3785c00a85c8ca8fd329c2a8a53c1f5cd8865
# Thu, 08 Aug 2024 16:37:43 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:37:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:37:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce02d10b61bf34aa182aa7cd3783def4d5bbd8176c97011032c1508b214ff88`  
		Last Modified: Sat, 07 Sep 2024 08:43:43 GMT  
		Size: 987.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc2a136d16381dd1cb44173056502b63f1221519780ccd6a68b144efc25d984`  
		Last Modified: Sat, 07 Sep 2024 08:43:43 GMT  
		Size: 1.0 MB (1047249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ca8946873e79c55e98d72c8e8199b4e5fa08d6d8c68ef8a6901d7c0300fd2`  
		Last Modified: Sat, 07 Sep 2024 08:49:49 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e732be064c163369f8060a02cdb4896b04c1cdb30b10c1a5bb161a03df18d9`  
		Last Modified: Sat, 07 Sep 2024 08:49:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9726eb4bf66ea1b549d7e9c8ad8ea5d2fb9006f51e76e64d344f855d51988c36`  
		Last Modified: Sat, 07 Sep 2024 09:06:37 GMT  
		Size: 88.0 MB (87961017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86304cd17fe54ec987c4a0e7a0eaa4e60ef60ad3f62c22abe4c88556dfe20e71`  
		Last Modified: Sat, 07 Sep 2024 09:06:34 GMT  
		Size: 9.0 KB (9016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c2c5eecdd109a6fc63010f5c4d8a7f8b04cbb0b9dea8618705e90b9d37749b`  
		Last Modified: Sat, 07 Sep 2024 09:06:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eada43e0b0757a46bbf0bf06d065d87d47644bf0f1c64e84181c8c2dbe0a5b`  
		Last Modified: Sat, 07 Sep 2024 09:06:34 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c54e2be3f56cd014de74cb5ba8b81d8607fc2e6bd83165434ed75347bbfd4b4`  
		Last Modified: Sat, 07 Sep 2024 09:06:35 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e45afcd33b30dc08b37f524e347cf1599017603b6387208ac20887657dbc8d`  
		Last Modified: Sat, 07 Sep 2024 09:06:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:ec962d4cdfa492680fa93976644e474b8e8bbbea2ee26a7e39cfe11101e36dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.2 KB (633230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438a16a9a15b9b1a2d03a69e3ff5f46511a66dab98f407b29b38c2ba5daa14de`

```dockerfile
```

-	Layers:
	-	`sha256:51b5e6f672fe5e4cf4c592ddd47ea541cd2819c7f0e76a42f922e465dbda95fb`  
		Last Modified: Sat, 07 Sep 2024 09:06:35 GMT  
		Size: 587.8 KB (587811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61f12471804c0223aa6c2dd1a7322c6d043e614b6386b814ad605bbbf019b53e`  
		Last Modified: Sat, 07 Sep 2024 09:06:34 GMT  
		Size: 45.4 KB (45419 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:e1a627e7f98a4c06b4532cc52ca286ceca3169e69255fcc496448116e3eef41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101221200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb795b36cdbe1a2078cf9581e4471defdaa6a49e09456ee1481227af8c3ef24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:37:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_MAJOR=13
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_VERSION=13.16
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_SHA256=c9cbbb6129f02328204828066bb3785c00a85c8ca8fd329c2a8a53c1f5cd8865
# Thu, 08 Aug 2024 16:37:43 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:37:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:37:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7628303f9a7a4f5bfbb9ffd0fc798dc56f9f31b015d69a05aeb5c79c712bacb`  
		Last Modified: Tue, 12 Nov 2024 02:39:16 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f8be78e67ddae659dfa3a3c81d0e6db6fd1ff30961e8d9cb03102e44b4fd74`  
		Last Modified: Tue, 12 Nov 2024 02:39:16 GMT  
		Size: 1.1 MB (1094868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cd57abb027525bb2e8f79a232ec206df6f09c9aedd0920e9a3c164af4c3020`  
		Last Modified: Tue, 12 Nov 2024 02:39:16 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019b55618c7cb36bce4aa94c76c04de4464e223251254e1c3d462d35b29c3bcf`  
		Last Modified: Tue, 12 Nov 2024 02:39:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6066da1d870a0217ec296e24bfff385795f2267f051e39c593432744f5cebbaa`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 96.6 MB (96640919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6219f9d0216ac6d3ab1be0a12e0bc1e1b01fd072838144a5e449a1b450def6a3`  
		Last Modified: Tue, 12 Nov 2024 02:39:16 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce706498fe01a769d14af6dd91d8b8bf3a7941de5e68d53b499a19bbfe094a1f`  
		Last Modified: Tue, 12 Nov 2024 02:39:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e82e44c19d5f071f59c522131232547a811ed4d0fe593686ce94d0173f571d4`  
		Last Modified: Tue, 12 Nov 2024 02:39:17 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9965778765683cbb63e0d87dfb97ae7dc385241ce8310eeaa68ac84bb04b9b`  
		Last Modified: Tue, 12 Nov 2024 02:39:17 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da74eaeeeed33cb6ea77422a7639d714f8f6a3f002714a7a6a2828b12e703d4`  
		Last Modified: Tue, 12 Nov 2024 02:39:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:b0ad6e762db7c4869823d5149669525a366596299b29bbe783bc1581553943ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.3 KB (633310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a83d3f37f241ec5b076cefab1f9d5cd48f1c64e6483c684f1a1fdeab5a276b7`

```dockerfile
```

-	Layers:
	-	`sha256:faaad2066e561bb3b8223a6751d7fd81cc77caeb613654b5d42dd3ace62c12d6`  
		Last Modified: Tue, 12 Nov 2024 02:39:16 GMT  
		Size: 588.0 KB (588048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad964cd8a0ef38b91162eb1546690e30fb9efab5e1c44a4710ad5bcc0c4dda6b`  
		Last Modified: Tue, 12 Nov 2024 02:39:16 GMT  
		Size: 45.3 KB (45262 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:57abafc036fdff594cd2da2b8b0856f61d2230725a17eb0431610b148de21311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.4 MB (100388437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b907f303738143b1591d30f606cb9ce6ee49887ba8c805bb1bb95a49c38edd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:37:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_MAJOR=13
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_VERSION=13.16
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_SHA256=c9cbbb6129f02328204828066bb3785c00a85c8ca8fd329c2a8a53c1f5cd8865
# Thu, 08 Aug 2024 16:37:43 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:37:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:37:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19a7a1f04747157cc38c8ea66a5ff6b25a502c971bf6b56995e5fefa252c706`  
		Last Modified: Tue, 12 Nov 2024 07:00:20 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1f73e281b372894f9fde9cf8b361dac11c7e4a99a9be8741f261633ef51c5c`  
		Last Modified: Tue, 12 Nov 2024 07:00:20 GMT  
		Size: 1.0 MB (1037936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eacc863115d916c7f14fdb7956d45a06cd56072bfcb39abee699970ca8aff`  
		Last Modified: Tue, 12 Nov 2024 07:09:39 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f4827aec3ef0953d51b1267885e898aa3f3f28676e7230bb67120dd71f28c2`  
		Last Modified: Tue, 12 Nov 2024 07:09:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe541f8df9c3422d5bb4c0234a993713a34996e05ee8f0e95fa2f2e212434d3`  
		Last Modified: Tue, 12 Nov 2024 07:35:26 GMT  
		Size: 95.8 MB (95761846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64ffd330b17cb9d9c706a39364a9b64729b3b4757d52f8f62f1b5d5981ca339`  
		Last Modified: Tue, 12 Nov 2024 07:35:22 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abea5f19f5625fee74fba51544855a542e0be382a4d402f4cc441ba5d303458a`  
		Last Modified: Tue, 12 Nov 2024 07:35:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d34520943e2ec7e0dddaabef726a3fa139f6a077548065f2a2cd3a97b13c1`  
		Last Modified: Tue, 12 Nov 2024 07:35:22 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a36e3fcdfb6dea84aa542b7cf906f8013f532a465821ded1be2de87a54edaa3`  
		Last Modified: Tue, 12 Nov 2024 07:35:23 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8df8cea07f4ed4830bfbf03eaeb5062a2aa73d86033ebfc1fa1731a5d525ac2`  
		Last Modified: Tue, 12 Nov 2024 07:35:23 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:2de16a8f43076fa683b40d711f246a5bdc232adf20d95434dfc2a49c117f9441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.9 KB (629859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edd05a024874b4f8409f9188332c2f14bb602e37fcb64f7da65cf2300d407b8`

```dockerfile
```

-	Layers:
	-	`sha256:c3eb2c6118c548de9299ea55946bbab43b46b322a63d596020202a30711e4506`  
		Last Modified: Tue, 12 Nov 2024 07:35:23 GMT  
		Size: 584.5 KB (584489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e98ff801c3a1f16c2b76b28120ab2b07194dcbce83bd2a48219aad3578a2e1d6`  
		Last Modified: Tue, 12 Nov 2024 07:35:22 GMT  
		Size: 45.4 KB (45370 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; riscv64

```console
$ docker pull postgres@sha256:5c4ad78abbe3b31891a9bbc9b50eda58de8b69c58994558fbba09e81279ed2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94016353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10cf693c7c1647c5aed2ad8d1841f65eff8afd47a98b0c320bfdbd4d570d88bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:37:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_MAJOR=13
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_VERSION=13.16
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_SHA256=c9cbbb6129f02328204828066bb3785c00a85c8ca8fd329c2a8a53c1f5cd8865
# Thu, 08 Aug 2024 16:37:43 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:37:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:37:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c0a33ca1e0010b2933d844f58d1adbfedd0d5f9ed593d28f743f587da5c4f0`  
		Last Modified: Sat, 07 Sep 2024 21:37:02 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc8cc678fef78489c3aaa8bdfb1dcc8f823e88452890bd484cba0b49520c887`  
		Last Modified: Sat, 07 Sep 2024 21:37:02 GMT  
		Size: 1.1 MB (1087946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56080afd24856e1cc3534a3aa835dd8e919182dcbb4d29dec312b4b72463b1`  
		Last Modified: Sat, 07 Sep 2024 22:25:51 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6835e21d92909284f4c71469ba5da9d23258e4089d86e92014b58bd67c10397b`  
		Last Modified: Sat, 07 Sep 2024 22:25:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668b46aba23ebee25294c3adfdaf8dfd19097c1bae74f5f8f8c9d524dcdc9445`  
		Last Modified: Sun, 08 Sep 2024 01:23:20 GMT  
		Size: 89.5 MB (89540740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f5e7c989e07ab1b220ef4ed8f68d7d813b6d1e769611b38dc929b1813e5a32`  
		Last Modified: Sun, 08 Sep 2024 01:23:07 GMT  
		Size: 9.0 KB (9025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb42ae2f6305f28f204f0cfc1385e326b2589ef7d2e21d2c0e5c186e83eaad88`  
		Last Modified: Sun, 08 Sep 2024 01:23:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502b04561436bd019a868fee75543ea48acca64710b271aa91485ee6921f4fc6`  
		Last Modified: Sun, 08 Sep 2024 01:23:08 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723125f3c7eedc6eed1150149df080e36d236506ca8e420f734e114c35df7019`  
		Last Modified: Sun, 08 Sep 2024 01:23:08 GMT  
		Size: 5.4 KB (5426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0575fe4ea783cb893fa983007c65a2e8f2c4dd334ab2f6dfabd3a182e8e285`  
		Last Modified: Sun, 08 Sep 2024 01:23:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:f49c186e78dc5582f17db8dbd0dc0cae836933c3103107dd9a1160e877b779a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.0 KB (631004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c519b3d30a446c35d960ab0c60deb836377b1e1b82550f058825505b14e6d6`

```dockerfile
```

-	Layers:
	-	`sha256:b04a4095a1211f5ccd0756401987187f74f169c1b63e73543c392c03e305c249`  
		Last Modified: Sun, 08 Sep 2024 01:23:08 GMT  
		Size: 585.8 KB (585831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34d88db79cfc7387056201acd241d61185a5eb1f840c8bd1e7f95b939a4b498c`  
		Last Modified: Sun, 08 Sep 2024 01:23:07 GMT  
		Size: 45.2 KB (45173 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.20` - linux; s390x

```console
$ docker pull postgres@sha256:af50b5fe378aa8b87adb0751405a833d824e34ddb5ba9079e7cafed6fd8ccad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102654257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad1df37598900d30fa4a00095f6391e0c0089be560e6f78c485eb66436099f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:37:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_MAJOR=13
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_VERSION=13.16
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_SHA256=c9cbbb6129f02328204828066bb3785c00a85c8ca8fd329c2a8a53c1f5cd8865
# Thu, 08 Aug 2024 16:37:43 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:37:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:37:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bd51305a798a8f4a2548106c9ede18568dab62599f818ec4a568a640541969`  
		Last Modified: Sat, 07 Sep 2024 07:27:24 GMT  
		Size: 987.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77eb0b034a50a4f7c869cb4d64d60e371eca69a55c30006747fb3a91328aacc`  
		Last Modified: Sat, 07 Sep 2024 07:27:24 GMT  
		Size: 1.1 MB (1083302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ae0cd9e3c227f9e874d4fac08c444e3ac40d3b959cd6a3d31351ff1594907a`  
		Last Modified: Sat, 07 Sep 2024 07:37:08 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf72d40b4fbebd98d7ab2aa3e1fabbb60f08d02688c85979de76e743727ddc9`  
		Last Modified: Sat, 07 Sep 2024 07:37:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d02ceaf1be47c2244465e20621e86979a76837fda747f850cf8cb4e7ce3133`  
		Last Modified: Sat, 07 Sep 2024 07:59:20 GMT  
		Size: 98.1 MB (98093166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bfaf17ddbea0b689ce03adde180f7c25ad87a3adafc3c6a680066bff8c7a75`  
		Last Modified: Sat, 07 Sep 2024 07:59:18 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e143e9b005b5a3b2013de11f3f7787514155513b557af94560ecb2c5126104b`  
		Last Modified: Sat, 07 Sep 2024 07:59:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fc1616c0cd89e1cd9057d398ceb263c5f1dcf00f056f511035bfdec0a4c568`  
		Last Modified: Sat, 07 Sep 2024 07:59:18 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1ee68d5c03b239302cb8712f6e14bbfca5d096bb3eb792296a2d1ce5fddfa2`  
		Last Modified: Sat, 07 Sep 2024 07:59:19 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6650adfa027c2e56345bca9344aac803f411152f26cb152b60503cb6f51ded4`  
		Last Modified: Sat, 07 Sep 2024 07:59:19 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:632ae72d7e74a782a1edc07572637b0e5cd28b25ec8aaf592d43ac1a0a50aaed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.9 KB (630920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a799659449299758234a6e6ebdeff8008cb279f76779cecd8c32de07990377c4`

```dockerfile
```

-	Layers:
	-	`sha256:ca36e08506bb778474cb272a5a3efc52ac7aabd8bff6e521eea8de3ad29450a6`  
		Last Modified: Sat, 07 Sep 2024 07:59:18 GMT  
		Size: 585.8 KB (585801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2bde718eea01cd3c12b49d33b8f82847ccfd00cd06e8bd7cda13d86ef414e1d`  
		Last Modified: Sat, 07 Sep 2024 07:59:18 GMT  
		Size: 45.1 KB (45119 bytes)  
		MIME: application/vnd.in-toto+json
