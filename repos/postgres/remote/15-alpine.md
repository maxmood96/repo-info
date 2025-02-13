## `postgres:15-alpine`

```console
$ docker pull postgres@sha256:a58cec2ba7a60b4c08d51f2ca93c1ad65fbf96e75cf0c89b7c0d2684860d3bb3
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

### `postgres:15-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:976a8a8fe0a764d2dd012fcfdc814e6c4dc541b435a660180c8192f467b2fc86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108663425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2404745c5768be935748fbc9ad7f2c9784ed03242bffbfe2f08588d3f2829a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=15
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=15.10
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=55abe738d441f0e58658b3ec6f88097a713b5e3b73139f6230d7b5c4c389e573
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874c0bca40ddf1ca31152b8543d8c519908f371e872c0af708219ca1b2ad2e8`  
		Last Modified: Wed, 05 Feb 2025 00:11:09 GMT  
		Size: 981.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718e9e313bab1db4b8e2347589ae7dd8c2981c1dddf5556953dfb10ebb0894ac`  
		Last Modified: Wed, 05 Feb 2025 00:11:10 GMT  
		Size: 1.1 MB (1120325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7106d5444c568dca603f2735f74e9f11d2065ead091b13f0afd49b01e69b583f`  
		Last Modified: Wed, 05 Feb 2025 00:11:09 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6705a3220790602b55a02992d12e8a3d519ebcc286b8fc3965d7ce47283f54f4`  
		Last Modified: Wed, 05 Feb 2025 00:11:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0859ff246e7c72030a1c2bea46d0900680202e07f408428c9dd85f83b2719d43`  
		Last Modified: Wed, 05 Feb 2025 00:11:12 GMT  
		Size: 103.9 MB (103884784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f33b3a5fd10b4f7bfa632c6e6299a9591db64d0935a28ccb3240eaac74dca97`  
		Last Modified: Wed, 05 Feb 2025 00:11:09 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b5be0a541fb6c4d6a6587a2f7236af7759c08a91e4b81c6abbd629973a8858`  
		Last Modified: Wed, 05 Feb 2025 00:11:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8448227d34d45900567119b299339a185f3220a02e97c1d36916602783d5992d`  
		Last Modified: Wed, 05 Feb 2025 00:11:12 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb4b442ea1326ceb4219832faa2fb0f492eec2d139f6b31b818bdf531c302d8`  
		Last Modified: Wed, 05 Feb 2025 00:11:10 GMT  
		Size: 5.4 KB (5410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016292b1aaa6d4aca869d705c358376dfed2b14b6001fb342b57647bd9e0b503`  
		Last Modified: Wed, 05 Feb 2025 00:11:10 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:cf06dfb623f53f8e4499a088957902487675b041720b50b0df0228eaa496df7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.5 KB (640495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a10c8e17a4ea04278f2445bbd3fa2a1e344adbfff74584dc255eb105320e3b6`

```dockerfile
```

-	Layers:
	-	`sha256:88291813d8f285e2e1bbd9025ba1f35855ac3c3f9e2953f2f3fc0bf7ed523a18`  
		Last Modified: Wed, 05 Feb 2025 06:31:48 GMT  
		Size: 595.1 KB (595063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71fde6172cbb87e7a8a92a8fba26e23abafcfcc561e38174a8ab4fce0479206a`  
		Last Modified: Wed, 05 Feb 2025 02:04:08 GMT  
		Size: 45.4 KB (45432 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:4d518514a90648395575d2b65f444149d3799f1bfba18cfe4a913ad5d4ff068d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88315448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b482986452a878388712e95372a3e4a274f8dac4db5a179649bef8c7322ad03b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=15
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=15.10
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=55abe738d441f0e58658b3ec6f88097a713b5e3b73139f6230d7b5c4c389e573
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a22c557d31caf1b269aa223bacac912676332abc4327c4fc6d8db2708f4b85`  
		Last Modified: Tue, 14 Jan 2025 23:02:12 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958deb370f8f34e49786548df7ccce1178adf3085f56572db7da1fa3bdcffb3c`  
		Last Modified: Tue, 14 Jan 2025 21:44:12 GMT  
		Size: 1.1 MB (1086612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5baf854ce9dcfb4a9c9035f65fda2ede7e4341458462f603a1a2e5470a9497f`  
		Last Modified: Tue, 14 Jan 2025 22:31:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e858c75599abdf33031fd4cf16af58c3e650f1e9a786e6a125088aa5ab788f8`  
		Last Modified: Tue, 14 Jan 2025 21:44:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b582d7cb4c686b8d8056775053dbb0b79f2776021d83e241369210106a353b59`  
		Last Modified: Tue, 14 Jan 2025 23:02:22 GMT  
		Size: 83.8 MB (83848335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0271ceea3b6fe94a9f18c61ccd25ded842cbfb66d4a0123ba6740d89ae1fd0c0`  
		Last Modified: Tue, 14 Jan 2025 23:02:24 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f69d10187f73989172d8b461e8eee0e1d4504936c58189da5889c4615b09e8`  
		Last Modified: Tue, 14 Jan 2025 21:44:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172329d6cbddab6ebeb9649f02c3055a5f0f687abf55bd5d6b1fe7c27e489918`  
		Last Modified: Tue, 14 Jan 2025 21:44:14 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a369dbd4c6ee7a437cc255326b36521bf529bd1ac2e5b7d427a809123636a55`  
		Last Modified: Wed, 05 Feb 2025 03:07:12 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9490ae60cb705853f7c996e23904c0e65d8c462617819903339b85e4ff3214`  
		Last Modified: Wed, 05 Feb 2025 06:05:44 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:c59879a86abbed6f0b2c569f201c14b5cedd92430ca7ac56eade4086aa8509c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 KB (45391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d13aa8a2d75189728ec6b85092b8c2f6db82fcc960012f65477550af6c9376`

```dockerfile
```

-	Layers:
	-	`sha256:57efe8c0b67e72fec06eed046240415ef1a7535266020a2689a6a860d38c165c`  
		Last Modified: Wed, 05 Feb 2025 02:04:15 GMT  
		Size: 45.4 KB (45391 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:854a3fb5386587cfffeef5e6e588de969c406e9c6c87c39aadd0482006412fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83556527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528d8729e259159c12f03143cd8da23c3f4570e3e0d4b24f91d72f50d3f73782`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=15
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=15.10
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=55abe738d441f0e58658b3ec6f88097a713b5e3b73139f6230d7b5c4c389e573
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb05567add68abef3b484f37aa5bf5731fe13ff929e5e9771adf36091ac003cb`  
		Last Modified: Wed, 05 Feb 2025 00:14:05 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54474578abde0ef4c2fd9521acf2401673783619c7536bdb4da90ff27ef2453`  
		Last Modified: Wed, 05 Feb 2025 00:14:05 GMT  
		Size: 1.1 MB (1086604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3720a05cdbcb135123c80645f89293a7d4a202fa142272d381f2e1289dfb1e`  
		Last Modified: Wed, 05 Feb 2025 03:03:02 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01033150115b824d062d4b717c707bca61d5c831145259972b7c78035a04e960`  
		Last Modified: Wed, 05 Feb 2025 01:29:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e924c939134ef8f42411d5a902a4f246e78559e6f6f9971205edea2c7ea04a`  
		Last Modified: Wed, 05 Feb 2025 00:35:53 GMT  
		Size: 79.4 MB (79356187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662d7903b08317d6150ec5032b594efe0e39afbead6c86174bafdd902c9fb189`  
		Last Modified: Wed, 05 Feb 2025 02:04:24 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667444b99081df833524244b763d7b4c036aa32c6604b139dec77ec218b97198`  
		Last Modified: Wed, 05 Feb 2025 00:32:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b6d1d3d5927ca40d7194c68136e9329382d77b2f9a407712d992eaddd6ba28`  
		Last Modified: Wed, 05 Feb 2025 08:00:18 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bde57e63ecd3a4aa295b5f6512680d7bfac4956f849e4b7af441252da4ba4f`  
		Last Modified: Wed, 05 Feb 2025 00:32:08 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5aca5a29ff9e7175cb62358e16e17ad906029b002eaa297f04544750035836`  
		Last Modified: Wed, 05 Feb 2025 00:29:40 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:40a56611ad3b82ba1be3c5b0f617cd76f9e518eae4afd0887c6171afb4ed07ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.7 KB (640705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998c09831e97dc4e7ea3bc67ea5b4aa28cd6977f10836384edaa09e18b7e6e2e`

```dockerfile
```

-	Layers:
	-	`sha256:a3047e380e49eeb6d34463c8bfac314e30bdfbc854330fc0d96fbf631242cc00`  
		Last Modified: Wed, 05 Feb 2025 02:04:32 GMT  
		Size: 595.1 KB (595099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57bd3c0fdeea7ce8f98aa25dd14dda86b658aab323d384e973bbf7c9a86944e2`  
		Last Modified: Wed, 05 Feb 2025 08:00:20 GMT  
		Size: 45.6 KB (45606 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:aede09e687a9e9a796cd96e4f78abc32aa96b0cd10db948308f2c3a5e97d2153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104548103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6656aca5af99ed2af2497d1e9ee0d2433a96148efaeb32a352555f68310c4d9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=15
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=15.10
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=55abe738d441f0e58658b3ec6f88097a713b5e3b73139f6230d7b5c4c389e573
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992b9109aeaae74f5c47c852d266a21087868b3d59823c415cf47660a048712a`  
		Last Modified: Wed, 05 Feb 2025 03:01:00 GMT  
		Size: 982.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9293d9b0151377c754cdc3169946ddbaf0bddd7c586d8fdb349913743b3bb2`  
		Last Modified: Wed, 05 Feb 2025 03:08:28 GMT  
		Size: 1.1 MB (1050045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d0e6790c6b5379712518ef114f466bda510f0c88ca89c5896e1bf3f4653e37`  
		Last Modified: Wed, 05 Feb 2025 03:01:00 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c31f786a65552f0cea52bf6c67821e98c1e19741cc1ede745dcc5607bab2c0`  
		Last Modified: Wed, 05 Feb 2025 02:40:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9e86cf3f03df2664907ccd646464fed73cbdbf005c0861fb6ed73117c706ae`  
		Last Modified: Wed, 05 Feb 2025 03:09:32 GMT  
		Size: 99.5 MB (99489079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009d48ac95fc2104286f97e650b33732efa9f519119269568911d503e52000c0`  
		Last Modified: Wed, 05 Feb 2025 03:09:17 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c9d80daea6267ae19bdabd2c4896eaeefbc844333b2a4cc516d0694f049062`  
		Last Modified: Wed, 05 Feb 2025 02:40:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1796b0769dd6123f565f69855f805655338df0b5dd1df2c351db411002aff624`  
		Last Modified: Wed, 05 Feb 2025 03:09:30 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e02de7f365c67a382c1c6fc9de99de9a86dcbfc8833bd3b07a384f7a39b29f`  
		Last Modified: Wed, 05 Feb 2025 01:12:14 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec009dcd7b437aa5805184e5aea35d43dcf794f080e4a5e1a7abf95aefa12fa`  
		Last Modified: Wed, 05 Feb 2025 02:40:56 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:4ed1c311a6812fdf93123960ac1da988d04415843087da9cec41dcf0ef28817f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.8 KB (640769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfe0f227dbd6cf28e91b3d7987dfca2c9041b47e8ac0e3449bf4d76c43c8bab`

```dockerfile
```

-	Layers:
	-	`sha256:44c118c86f46799dcd6c64194b9526341f26d82db9dc8f029be914e9f7ab7c99`  
		Last Modified: Wed, 05 Feb 2025 07:05:21 GMT  
		Size: 595.1 KB (595119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d3f89a7a62292a21c04e5acc52703c8328556ec587bbb944bdbe86456fb1b93`  
		Last Modified: Wed, 05 Feb 2025 07:05:27 GMT  
		Size: 45.6 KB (45650 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; 386

```console
$ docker pull postgres@sha256:f8470f00c48fc31984d6f8b87aadb4bda6685493877143eb6cd406822109d3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114809046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fcfbfbeba34639266215d2be6acf7867c25f7755d774719cba376ea6454614`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=15
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=15.10
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=55abe738d441f0e58658b3ec6f88097a713b5e3b73139f6230d7b5c4c389e573
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46be37bd8dae9d7196a9f55e30843af30a17310af85d55a7dc3170de2d6d2edf`  
		Last Modified: Wed, 05 Feb 2025 02:04:37 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109e044aa6b72bd6ede7f87466beb72998331ef19c794c15b15972beaa2724d4`  
		Last Modified: Wed, 05 Feb 2025 02:04:39 GMT  
		Size: 1.1 MB (1095272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56673d42c38af622a7b6a48c1e28668e6c552960e916a09c87e21812f3614af`  
		Last Modified: Wed, 05 Feb 2025 03:07:14 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4261608f05b70a27d187fb5cec036396930c7f5c899c2ec2190e262ccef615`  
		Last Modified: Wed, 05 Feb 2025 00:18:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30150b2e44577ceffb2a9685ba88f29766d6b2b87b9a87228339861c2120ea63`  
		Last Modified: Wed, 05 Feb 2025 13:02:46 GMT  
		Size: 110.2 MB (110234044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1318d236091bf1070e89351891f946005ea196e64907b940b6c769887cafdf`  
		Last Modified: Wed, 05 Feb 2025 00:18:35 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608480d6a7b307a37b27282822d4de60607d311153a95e946fed394b43f94e5d`  
		Last Modified: Wed, 05 Feb 2025 00:18:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787d70a7d28b00fff8ccd0e7e1d6b24fbbb91d16643e994e28f1439a6f134895`  
		Last Modified: Wed, 05 Feb 2025 02:01:52 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37099af704a65e3c3fa82dc007b8e1cb9e5c4dbd9725af9798cd4be955a4ed51`  
		Last Modified: Wed, 05 Feb 2025 02:04:46 GMT  
		Size: 5.4 KB (5413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787be20278a28b3d0c73c63470e730973b3fc0a8cd18d6aa05b5dca5577e9326`  
		Last Modified: Wed, 05 Feb 2025 00:18:33 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:5d4cee7851cfae40d58c2bf07304afe5bf395e7310949f66f23d63b2e82fae5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.4 KB (640422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e527b7bb051cf2eb4b857d7316591c0185db297f23f65b486598502bf8e4273c`

```dockerfile
```

-	Layers:
	-	`sha256:1cc34f5c96203d3f21c83eadf662a4c864c1139131454c0384741c6924d6e901`  
		Last Modified: Wed, 05 Feb 2025 06:32:05 GMT  
		Size: 595.0 KB (595038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55c04f3a478a875e67e670acedfee94b257ea97e19962cddb3ba9487f5ceaf65`  
		Last Modified: Wed, 05 Feb 2025 02:05:10 GMT  
		Size: 45.4 KB (45384 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:b7f2eb8905c88dc78c63ba38e65653b6e72a8d9aa1c84759a2ecd67298100d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92375293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1e75229fe0780813b456ac662a539b4663635c566bdd2d8abdff80961c6226`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=15
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=15.10
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=55abe738d441f0e58658b3ec6f88097a713b5e3b73139f6230d7b5c4c389e573
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4de803835da75ae4f48f846b265f10fed54358c260b7dbb0f1bf1e98ed04943`  
		Last Modified: Wed, 05 Feb 2025 01:01:59 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e88bb7ce399fcbab123a0a9f8aa3b30e35ba5b27750c59aff36e4a681dc5c1`  
		Last Modified: Wed, 05 Feb 2025 01:02:00 GMT  
		Size: 1.0 MB (1040364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b752c49809654d9c49698e50bbd5df99153af5a326ca0bbc54a4203ce43ebb31`  
		Last Modified: Wed, 05 Feb 2025 02:02:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e2c352c662ba8f20316b983b960e9444231e8b4ef47c78123841ba5bfbad37`  
		Last Modified: Wed, 05 Feb 2025 01:07:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d8094f8d25dd661066ecb44bb15b3f7504707141e4018bc7ce12f7cd86959e`  
		Last Modified: Wed, 05 Feb 2025 03:07:21 GMT  
		Size: 87.7 MB (87744705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f877676f6ae0281ec8e659548d145d36281d1a1b0b171f9a8d1a3a40420c29`  
		Last Modified: Wed, 05 Feb 2025 06:17:52 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f546b1070110d5ed7ef7f342470eb077a629e9e90f0e453d75505058d244856`  
		Last Modified: Wed, 05 Feb 2025 03:59:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a344ad514de973da70196d5c8003e536b7adc4bfc060cdf630f01ac2b716ded`  
		Last Modified: Wed, 05 Feb 2025 10:08:35 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4f5d416b17ff37a6e1a19bfebc31f7e80b0beb365b12aa412353978b867482`  
		Last Modified: Wed, 05 Feb 2025 06:32:07 GMT  
		Size: 5.4 KB (5413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4c9b11003fa1f6fd8e0e57a97d84117bfb544f49707c40fe1fbf96e8d11d9f`  
		Last Modified: Wed, 05 Feb 2025 02:05:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:33dd4a36d7de652fddd516f6558c34047c3457dfd695e85391836a9e77e73cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.0 KB (636970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12064e5c7fcb9d47baac417852c2ea76b003e1ca8df1a93a797dabede92fcfd7`

```dockerfile
```

-	Layers:
	-	`sha256:7081b40b9d193360563f12e66453d47d3241bb73e397ad287c273a4c2c90894e`  
		Last Modified: Wed, 05 Feb 2025 02:05:24 GMT  
		Size: 591.5 KB (591484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7db4e07e2d272ac4b42140cb8398ade3dcc611adb3f1cb1c1ad56f1e09a03bc`  
		Last Modified: Wed, 05 Feb 2025 03:07:15 GMT  
		Size: 45.5 KB (45486 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:ef845a98193893a1fa0b446c82447d9b0e0c36eaa28da34eb34f343228087bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108617869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b29775f1bf9e6684553cbc4de969ffc65b25cd80bb9a94fa876296f135a2cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=15
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=15.10
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=55abe738d441f0e58658b3ec6f88097a713b5e3b73139f6230d7b5c4c389e573
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa70428e43128e29ea85c02b9ad8867c57f3c57d80ee4c8367e06d1044bc81a`  
		Last Modified: Wed, 15 Jan 2025 02:15:04 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b30861d9a22965c9c8ab0e3148f19b31c48adac4184db37373b16aeb1836e26`  
		Last Modified: Wed, 15 Jan 2025 02:15:04 GMT  
		Size: 1.1 MB (1089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ee96017ef0ba8a5e5adc67c305a2bb47d5c776594a60202ef59765710d8a19`  
		Last Modified: Tue, 14 Jan 2025 23:03:24 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ecc705b39b2ca8d6e5ca7d9227c696d64688b012cc93494869f3a75ac26b68`  
		Last Modified: Tue, 14 Jan 2025 23:03:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af6237683b5ead830e1f1fc08c62d0b74b3543eedfb2f5312eb5e6849fd3b54`  
		Last Modified: Wed, 05 Feb 2025 07:08:37 GMT  
		Size: 104.2 MB (104161182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2962203bd819179d1152d7a24b47e2168327ec45d8b144610c18ce348e5793e3`  
		Last Modified: Wed, 05 Feb 2025 13:02:38 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e4d241cdeb2712be317a5b34af56372c2ac3eea599f97a97678b796f168822`  
		Last Modified: Wed, 05 Feb 2025 04:00:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed2694a6098f97c0f181840847831088c245be03733fcb7aad3f48e4adbfc04`  
		Last Modified: Wed, 05 Feb 2025 08:55:02 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8484bbed027bd874969b12bdbfd5058a97485988d5d87d50021d7e45e0d00b5a`  
		Last Modified: Wed, 05 Feb 2025 07:09:09 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5bf7ab6e24e3a6462dc441c209075951e2b20de162d7e1e36dfc96ace757a96`  
		Last Modified: Wed, 05 Feb 2025 06:21:14 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:db3831ffd72142b3202f760b631c15338bf6e3fc3ac4701dc5a83f0953a183ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.6 KB (638633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d5a696029ee75d3ebe5d82f73a5804e61e4304e3e0e8dd312c2feebea52557`

```dockerfile
```

-	Layers:
	-	`sha256:6262eac749ee2ee17d3a3f72f7c3e7696135827d2593632be0a6b31644f1af5d`  
		Last Modified: Wed, 05 Feb 2025 08:00:38 GMT  
		Size: 593.1 KB (593142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de2223bb5523ad1001b38b9dbe4aa419cbd33a3bc912d34aac83e90fd46f4178`  
		Last Modified: Wed, 05 Feb 2025 06:32:13 GMT  
		Size: 45.5 KB (45491 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:8414278ae97043b35f2ccdac7b487e1c1e8690100621edf56b4ab824ff29c397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117220917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b579bf4c8fb5baaa4cdfa0ee4a3848d7e9f3b0dc261d843d89580170f58a37c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=15
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=15.10
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_SHA256=55abe738d441f0e58658b3ec6f88097a713b5e3b73139f6230d7b5c4c389e573
# Tue, 04 Feb 2025 00:55:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c56695c85edb37ce406b4667f090721587f7d2dc9452e0ec86dae6902585d0`  
		Last Modified: Wed, 05 Feb 2025 01:05:37 GMT  
		Size: 982.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4ac9ad3604d910dc8b794cb00cccd50d1a63d5ec97b3256b4a8d034e01945e`  
		Last Modified: Wed, 05 Feb 2025 01:30:57 GMT  
		Size: 1.1 MB (1084567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae6505784918dbcf00ac2a80ef08d1b47355616628edee04c6679dbab5f4083`  
		Last Modified: Wed, 05 Feb 2025 01:02:40 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4b1780e171a060bacf653b2becb7b116054fcde6d16bdd688463bb751452d8`  
		Last Modified: Wed, 05 Feb 2025 02:02:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495ff69dc3e649229292e3a4c719ee8a83023c30c25e6356f587099b7fb48b56`  
		Last Modified: Wed, 05 Feb 2025 08:02:17 GMT  
		Size: 112.7 MB (112652865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4fc1feb9dd1da4fb2377b9fa9ac32c97efb6d8f4670a40297e69ea706fcdfe`  
		Last Modified: Wed, 05 Feb 2025 02:05:31 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fe4db57a298825c73917be989f019d9f1830f9b625cf5e26bf772199637fa9`  
		Last Modified: Wed, 05 Feb 2025 03:07:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc24eb194d69a693ff4ca251b849631a59e594ae54c4347d25539f7856cadea2`  
		Last Modified: Wed, 05 Feb 2025 04:00:43 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e673d6027e1a4d9d80af27747ec93063b5f57c5bb2fe53f785ee3a0a414809ee`  
		Last Modified: Wed, 05 Feb 2025 02:05:34 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9253689095f86bb1195edcc82a447bee843250d9ae86f146fffcb7f36759a6`  
		Last Modified: Wed, 05 Feb 2025 03:07:17 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:7af392333148e4c287bf353da6b63fedd1b5f355056561998cdb5576b0d4b192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.5 KB (638544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e68c510e93f1dc10bef72dfaaa69a54787cf9b5c40a56d2fa6fec2907b7c02f`

```dockerfile
```

-	Layers:
	-	`sha256:67bd4a3b0717630ea72ec7ac869a0e694a13f78ce1db38dcd023363e70c85505`  
		Last Modified: Wed, 05 Feb 2025 03:07:16 GMT  
		Size: 593.1 KB (593112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7d85244d84dbdd19fd2ac29f265b3cf75eaf4bea6691d313415fb936036e09d`  
		Last Modified: Wed, 05 Feb 2025 10:11:47 GMT  
		Size: 45.4 KB (45432 bytes)  
		MIME: application/vnd.in-toto+json
