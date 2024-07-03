## `postgres:17beta2-alpine3.20`

```console
$ docker pull postgres@sha256:9792901103820bcefbebd5fdd5424490972bf33208d88d2abe7afab6e57394d7
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:17beta2-alpine3.20` - linux; amd64

```console
$ docker pull postgres@sha256:8fc01f667c6d92ea6a7554be8387aeac9a0d6e16bd8ce701819a2576405b57c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.4 MB (100420534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f5f4e688fd21d817b67d2a0849f4bd4aa741b7711c255f185d89aa7dc3dc1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17beta2
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_SHA256=157af3af2cbc40364990835f518aea0711703e1c48f204b54dfd49b46cd8716c
# Tue, 02 Jul 2024 00:03:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834978104689c73565439f548f231b0cb11911aa702ce2b0c52b316d6bd258fc`  
		Last Modified: Tue, 02 Jul 2024 22:11:19 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6988546079d73496683f4a33a92312974b4ba4afe318e8eb111a149ada59ed8`  
		Last Modified: Tue, 02 Jul 2024 22:11:19 GMT  
		Size: 1.1 MB (1120074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186dbf9597e0519422a8c4f7c0ceecf425e5ca5d98b1508b7bbf789931388dc8`  
		Last Modified: Tue, 02 Jul 2024 22:11:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b101ba8edaa37fcc783e4c5f018805244c84cce6850ef699784b9406a288fc98`  
		Last Modified: Tue, 02 Jul 2024 22:11:21 GMT  
		Size: 95.7 MB (95659737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9d180e11d43ad84fee5bf5a252f289746d4cada7a3f193ee58819614855815`  
		Last Modified: Tue, 02 Jul 2024 22:11:20 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68a3452dd5eeb57ab529e85e449dec4aaf8514f04dc51dce54c1d20d51f9ff2`  
		Last Modified: Tue, 02 Jul 2024 22:11:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9f5557cc401a4a40cb802f50a24bb2fb02cf67337c0b9b3b2977a9ede31523`  
		Last Modified: Tue, 02 Jul 2024 22:11:20 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5bed6482a9f4b85a49701ba21abf9fb8d6598be0c5a041c95091ff2e17820f`  
		Last Modified: Tue, 02 Jul 2024 22:11:21 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96436df7ab4f3a9ab088708a1e03b054ed5bc41aee55ec21b6a8af6ac1eb6c7`  
		Last Modified: Tue, 02 Jul 2024 22:11:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:d6dd17d19ac59ee555c2e2c336a53d48648d187209fdc67aac65604acf69a19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.7 KB (622665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a32d82c070fbe6956db9ef322d2cd07e89a808d9069a868509b26ae41e0f5a6`

```dockerfile
```

-	Layers:
	-	`sha256:8e5a8f13c80b115022006c128f8a01fc003f7b094446adc44bce70bea435f677`  
		Last Modified: Tue, 02 Jul 2024 22:11:19 GMT  
		Size: 580.4 KB (580443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae5799bd6f4187e8d11242ff0914b347b6bfc455cec918bcf5279a9c26237aed`  
		Last Modified: Tue, 02 Jul 2024 22:11:19 GMT  
		Size: 42.2 KB (42222 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:fa1f6a9501bb369ccc0181a732cb31796b0e5111950a4e4b75a947252a0dfdf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98752300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d3e9a09ea6cac9247992b3cdd46b654bc94de43c87daf7da6a1b4aa70af497`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17beta2
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_SHA256=157af3af2cbc40364990835f518aea0711703e1c48f204b54dfd49b46cd8716c
# Tue, 02 Jul 2024 00:03:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab55c6243def97b76d41db1a4ce10d19488d1433a79078f9d4dbf5d4c0aa60e`  
		Last Modified: Tue, 02 Jul 2024 22:29:21 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f904f6b0fab460cbe01819613bb99846a5ef5e029ce537ddb987b103a059ec5`  
		Last Modified: Tue, 02 Jul 2024 22:29:21 GMT  
		Size: 1.1 MB (1086570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2d81add609dec4e955f0a9eb7be59b9c8625c6a8cdc2d61ce2a8b3c3d0fc1b`  
		Last Modified: Tue, 02 Jul 2024 22:29:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00711b1d09f5822063feeb86d78c6004729aaa90db6b2cc2df433d096ca131ee`  
		Last Modified: Tue, 02 Jul 2024 22:29:24 GMT  
		Size: 94.3 MB (94281696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e41755f67084076cadfcc94b46c80ad632d3569e08a2f6c391d25f564c59f63`  
		Last Modified: Tue, 02 Jul 2024 22:29:22 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117b9e1e1b27c0da655681dc99af59b3ba201974b27906f49f312963d2255569`  
		Last Modified: Tue, 02 Jul 2024 22:29:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0bc2a21a7e8bc9d58670e48afb19069ac7eeed97baeba9b29cb8bf76f0acef`  
		Last Modified: Tue, 02 Jul 2024 22:29:22 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789b4d309bdfbc23b496ae58c80c9f15f93b1baac2b56afcd5f1da34ee3a2acb`  
		Last Modified: Tue, 02 Jul 2024 22:29:23 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7f36bf3e08dd3c11347fc42b892dd1c26eb4a46556a1643ea6d81b1d686319`  
		Last Modified: Tue, 02 Jul 2024 22:29:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:d7f23414f9ad890d366f753f91f3230e17109bc19cc85ce8cfb2cdf90ed7b88a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 KB (42148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd35f3b0b18ebdd9332ee23d3921e80e1e69ac3d0a2b80703f087d1ad338c932`

```dockerfile
```

-	Layers:
	-	`sha256:c8823c1e54d1eb356ed9555308797c98854336a794d1929d758918071c48b896`  
		Last Modified: Tue, 02 Jul 2024 22:29:21 GMT  
		Size: 42.1 KB (42148 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:6b2adac2c580148900df80a87f86062fa25f4ebd35e7c5ec5110c8a8ca55b416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (92980100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9834da0568e5ed785753eee963bb89de0f0337a776c56a0197e9d821550b61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17beta2
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_SHA256=157af3af2cbc40364990835f518aea0711703e1c48f204b54dfd49b46cd8716c
# Tue, 02 Jul 2024 00:03:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81553e1165005635b89362e9d30f9213439a3722d973f49867d44919fa01a25`  
		Last Modified: Wed, 03 Jul 2024 04:59:14 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e46d57edca9e417f08bb85315398fc61028f4c072e910b276aa47adb0a8a1bd`  
		Last Modified: Wed, 03 Jul 2024 04:59:14 GMT  
		Size: 1.1 MB (1086565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aace4b8d49e556b7e126e481873cc92a31e6eefe9bbca1cab2624326b5cf3817`  
		Last Modified: Wed, 03 Jul 2024 04:59:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477884ad33c4d7e96cc4f4d231119325c320d1e6c258416e8c6397ec38c0b747`  
		Last Modified: Wed, 03 Jul 2024 04:59:17 GMT  
		Size: 88.8 MB (88781794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d57d2e92600e5d8eb11bbc0e61e087781cb9ab0e8360107747945429b4761`  
		Last Modified: Wed, 03 Jul 2024 04:59:15 GMT  
		Size: 9.9 KB (9886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59eec5533cbd8d8dd75aa484723ae3d208be34e0ca7cbabaeda692cd630a49e`  
		Last Modified: Wed, 03 Jul 2024 04:59:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86989cd25cd8a78c5429326856bbc2c71c7f2534056e6cb931507c1add800e66`  
		Last Modified: Wed, 03 Jul 2024 04:59:15 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd3263c8b09194f41cbd273890f16dde13416fe4a3c10863d1abcadfd2abad6`  
		Last Modified: Wed, 03 Jul 2024 04:59:16 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6ac65640022f5d3815ca7671e3b5c0e89ef6bbffc247ca0fe7ed9ae1141a15`  
		Last Modified: Wed, 03 Jul 2024 04:59:16 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:1c0b6522e69396dc9a1c1f3fc32162a2e25108bda82c811375e35810b29ad047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.8 KB (622828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b000e99910a896309020f28389f96d0dc69ca37566a7ecf2409c0af0a49a66`

```dockerfile
```

-	Layers:
	-	`sha256:17caaed77d7cf0ea7399cd2946553257372c6b5e5325141ea192baed525aaeb8`  
		Last Modified: Wed, 03 Jul 2024 04:59:14 GMT  
		Size: 580.5 KB (580463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:decce5a0f5cdaf3c80d603062f86d9cc177ad33f764e8db2266701d7d189e121`  
		Last Modified: Wed, 03 Jul 2024 04:59:14 GMT  
		Size: 42.4 KB (42365 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:d7cc162e448152184774b79f5408901279ee193d70a5a604ace50508d7beb563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (100040694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e9ec7bc58b86a32041ac2eb2dc0b5e4f6352a4e4830ade744ad1725c33a27b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17beta2
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_SHA256=157af3af2cbc40364990835f518aea0711703e1c48f204b54dfd49b46cd8716c
# Tue, 02 Jul 2024 00:03:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b761177dccad7911a3ecc7c08f28d96bddce0dd8cfdf40940789b949f478421`  
		Last Modified: Wed, 03 Jul 2024 03:59:22 GMT  
		Size: 981.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d92b590ff0e6485ccab3a28fd1cad698ac7b9f725d512515b27eb4de5491af9`  
		Last Modified: Wed, 03 Jul 2024 03:59:22 GMT  
		Size: 1.0 MB (1048691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905bd7f09a051afa9c465e76f092ad6f7b70b4fc5cec0550f7cd368e41376759`  
		Last Modified: Wed, 03 Jul 2024 03:59:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c19ddc549ceb9a3deae6c0f8d7e61885451b6394f18c1d731a684208398b4b`  
		Last Modified: Wed, 03 Jul 2024 03:59:24 GMT  
		Size: 94.9 MB (94886319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cfc4fe04bd117a2c5551d945924a0c2a5951decdaa864aaaad6e75f1fcd82e`  
		Last Modified: Wed, 03 Jul 2024 03:59:23 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5682c8cca407360ceb08ecc5d8069ff2569570693143c99ae37c2bbd2ec725`  
		Last Modified: Wed, 03 Jul 2024 03:59:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f22c3a1ece4bc50839eeecde8326f49410d0e42d91414c58115aca5a3ad4887`  
		Last Modified: Wed, 03 Jul 2024 03:59:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cff5a1532108ac91975d2944cdcdbf258ef584893ffc7c801dfd458d5cf1904`  
		Last Modified: Wed, 03 Jul 2024 03:59:24 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb50e5d689d915db36e7211942d8d3c8fde2297693d0761db9868054f17119d6`  
		Last Modified: Wed, 03 Jul 2024 03:59:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:879c6882a228665b895441f4dd426d86c649801c0d2678e092ca8eab943a7e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.0 KB (622972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3785fb1cbcd4765c2fa506b956770265752e8364bf95e74e2ca90709be9e83f`

```dockerfile
```

-	Layers:
	-	`sha256:c94729bdeb144e2d5c6d7967357f54696a809ec26fbeaafe46ba057e0d1980c9`  
		Last Modified: Wed, 03 Jul 2024 03:59:22 GMT  
		Size: 580.5 KB (580475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3af8d1e90e04dbd4e56ae1a0153b2779962b1f90c35c759b67e42742f9f17e0`  
		Last Modified: Wed, 03 Jul 2024 03:59:22 GMT  
		Size: 42.5 KB (42497 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:d0ddf1cdbd0c9a081b35d7645063fe53b9fa762a8dbe6ebddf976d137b0ccd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105599848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47356a57a13689d3beaf4ae29068049c01ca7960506b83e3f96eff3ca2e6540c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17beta2
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_SHA256=157af3af2cbc40364990835f518aea0711703e1c48f204b54dfd49b46cd8716c
# Tue, 02 Jul 2024 00:03:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3a6325dcfc33573d7083cd4ff63cb432179567938ad4c3b16d9b6d576210e0`  
		Last Modified: Tue, 02 Jul 2024 22:11:45 GMT  
		Size: 982.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f09825085eaeb133ba7493d6ce7f3515ecc322bdb082a0ad14bd18ece8fc717`  
		Last Modified: Tue, 02 Jul 2024 22:11:45 GMT  
		Size: 1.1 MB (1095334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186dbf9597e0519422a8c4f7c0ceecf425e5ca5d98b1508b7bbf789931388dc8`  
		Last Modified: Tue, 02 Jul 2024 22:11:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160ec631578cf9d2933618951cc646edade266d6e673498a116f6c04f960fa7d`  
		Last Modified: Tue, 02 Jul 2024 22:11:48 GMT  
		Size: 101.0 MB (101018161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ef9091357416505dd021dcf16e00d7492a4315ab403e73a559f8f4d2fedcc5`  
		Last Modified: Tue, 02 Jul 2024 22:11:46 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac2c598adef724315d7b69dac9705bfe4265edfc808d32c9caf8d4fd287f70a`  
		Last Modified: Tue, 02 Jul 2024 22:11:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd5768aba156ec5adbd730eff97ed6c3661342e91513345c748a552d7e6a7a0`  
		Last Modified: Tue, 02 Jul 2024 22:11:46 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9262fce9b9210f666ffd0f06111751306d910de2400d125bb2128d5f71640d21`  
		Last Modified: Tue, 02 Jul 2024 22:11:46 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da15fddccab75228e3927637e532b62be87e33f7d254bd29ae59a3958f533a4`  
		Last Modified: Tue, 02 Jul 2024 22:11:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:6e1277ffb2da15a48acd9f99062926f8067390434e1cb87448e33a7ddd2aa279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.6 KB (622623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b02659ab99c17e4cd0e98c05292b373ee10f3288c987530a50b07a5cc1eee1`

```dockerfile
```

-	Layers:
	-	`sha256:8d858309e9333b4259968059cb559488d63aaad001e1969510ab16927fb0115a`  
		Last Modified: Tue, 02 Jul 2024 22:11:45 GMT  
		Size: 580.4 KB (580428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:113e1dc402c8603b795366ae93fe4d36e65e5d12f1d68e1d78fcda25ef919902`  
		Last Modified: Tue, 02 Jul 2024 22:11:45 GMT  
		Size: 42.2 KB (42195 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-alpine3.20` - linux; riscv64

```console
$ docker pull postgres@sha256:09f4b88812b4d1f3a9e3f42967dd6a6c3c310b0a7b10badd0ee4932f6f1cd3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100229493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0b20fee5b9bb89ad9670ea8fec0de1facfe7e2f5208c3c8fcd76ed9179ff1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:03 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Thu, 20 Jun 2024 18:18:04 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17beta2
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_SHA256=157af3af2cbc40364990835f518aea0711703e1c48f204b54dfd49b46cd8716c
# Tue, 02 Jul 2024 00:03:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c58f5930149e76e139378edce2163384b6ac82b8bb8c88297a17355ff08f6a2`  
		Last Modified: Wed, 03 Jul 2024 02:46:30 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4faf557d98d802b9f83fc437ed671c73286c3f67a1f477238514367225d1150`  
		Last Modified: Wed, 03 Jul 2024 02:46:32 GMT  
		Size: 1.1 MB (1088924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc09079a1f03d224a6fd67def637ab0163a421190a12d1f9600a78b0e182bde4`  
		Last Modified: Wed, 03 Jul 2024 02:46:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57d1c553efe8dcef4ff0d86f919911ca36ece88b76e9262ddd0a5ca1366f7cc`  
		Last Modified: Wed, 03 Jul 2024 02:46:44 GMT  
		Size: 95.8 MB (95752634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04de37a13973319b292e6e9e64a1eaf78c0ad0e06f497c9d4aed65022f04124`  
		Last Modified: Wed, 03 Jul 2024 02:46:31 GMT  
		Size: 9.9 KB (9894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358cc4e179dc0f0b280fa03dcfde3dc9efcfb4858b85fe1f93246bfc7e24b722`  
		Last Modified: Wed, 03 Jul 2024 02:46:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b474b460564562f0b3ffef0c30662caf6395c8ddd4110caa425ed09d8f96a9`  
		Last Modified: Wed, 03 Jul 2024 02:46:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dd79075193f28081a74d25b00ffdd92c9e08db3ccb4f5e40dfbcd021901769`  
		Last Modified: Wed, 03 Jul 2024 02:46:33 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333350308cba87f87927898dd643b81e54ef332c4870da42a006b2436f65c4ee`  
		Last Modified: Wed, 03 Jul 2024 02:46:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:38f163d9601b6bde5107885078a6616dea734dd21e76f18fd5e9460b04b29ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.8 KB (620769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdd453fea30bed7774f8372818a60bbcda9849c430a5e2d07f72a6e53949f32`

```dockerfile
```

-	Layers:
	-	`sha256:4b2aec02e94f3f687cbac544d7024ce17b6ed8223fd1632269f70a164f2a9044`  
		Last Modified: Wed, 03 Jul 2024 02:46:31 GMT  
		Size: 578.5 KB (578507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0b6d1d478f8f93937a558c2cd7b33c1a5286199b7a9ed91330f5e150c6200a6`  
		Last Modified: Wed, 03 Jul 2024 02:46:30 GMT  
		Size: 42.3 KB (42262 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-alpine3.20` - linux; s390x

```console
$ docker pull postgres@sha256:2486f42bdaa23b765f6699e51ab2419a682e6159578a843801e6575d3ecc01b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109084583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69642c3b0199a383413abce279dbc763442f88e30ea22eb9b071c6f6b7b55306`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17beta2
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_SHA256=157af3af2cbc40364990835f518aea0711703e1c48f204b54dfd49b46cd8716c
# Tue, 02 Jul 2024 00:03:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3639f7b166760b64b0a7dea0fb09ff663614f6bc7e411f899476c0d1f9ead56`  
		Last Modified: Wed, 03 Jul 2024 03:28:36 GMT  
		Size: 979.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74eaa69cf5a348abc3c724aef09008cf431361ebefa6c32a1d392c148339486b`  
		Last Modified: Wed, 03 Jul 2024 03:28:36 GMT  
		Size: 1.1 MB (1083381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11d540e1b4ffe3f443efe79d330e595f4143e92e4e1fe4c628928b6943375a8`  
		Last Modified: Wed, 03 Jul 2024 03:28:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7771e4f7b26c74b0e01b4eb11fd2e120bb8d19bade73518fa71f567f6ee70a8`  
		Last Modified: Wed, 03 Jul 2024 03:28:39 GMT  
		Size: 104.5 MB (104522457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16303f655b66ce5aa3708efaa09cad3081ce71f0a8dc479fd98dfac316f8a776`  
		Last Modified: Wed, 03 Jul 2024 03:28:36 GMT  
		Size: 9.9 KB (9888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8921b82966407193317077e6db5cb5b6349222d287464b3cb2e0c436e6611a`  
		Last Modified: Wed, 03 Jul 2024 03:28:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabe65215b2490c26fd5799e3ab0875e6a44390034f73496f11a7ba07788e03d`  
		Last Modified: Wed, 03 Jul 2024 03:28:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a96ca284fc89fbdd1490abdcbe3157661336ae4d66b1795ed327da15ebeac4f`  
		Last Modified: Wed, 03 Jul 2024 03:28:37 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa127c65be47170fecbdb6c87306fe572d74a5afd4dd7e7bb03c73d386a6121`  
		Last Modified: Wed, 03 Jul 2024 03:28:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:4580262c572288bea959bd00678f97f2d212c06c5466d5f36a5bebc861ac18fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.7 KB (620717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9930059347c4a3713e6ba272cfab06050f31e6c840513769e15318ac963be0c4`

```dockerfile
```

-	Layers:
	-	`sha256:5529dbc53668fedf1f7d381918c02df8b297cea499c9023a288f450fb78c7634`  
		Last Modified: Wed, 03 Jul 2024 03:28:36 GMT  
		Size: 578.5 KB (578489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa7a8769953921815fbc63dab3d48e348d99a3af47a20f7a289cf0bc4b49aedf`  
		Last Modified: Wed, 03 Jul 2024 03:28:36 GMT  
		Size: 42.2 KB (42228 bytes)  
		MIME: application/vnd.in-toto+json
