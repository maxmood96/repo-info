## `postgres:13-alpine`

```console
$ docker pull postgres@sha256:2d286540b860707bc1e1027adb6c57380d03a9aafaeace8fd338e6c74db174c2
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

### `postgres:13-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:dc0ed3bdc9c279190dee5c2ccdb34b24e6333d34f9e89109bb370100de4d4e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106923781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a9cbca6dc5e5311a27253c6a45e3efb2b9344b5497112cf203adcb9dc214ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 13 Feb 2025 18:01:24 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:01:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_MAJOR=13
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_VERSION=13.19
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_SHA256=482cce0a9f8d24c2447cfc7b2817e55f86d51afe5f7f1a85214bf93644e774ea
# Thu, 13 Feb 2025 18:01:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:01:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:01:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:01:24 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:01:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:01:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b4a970a19d8dd6e7bf7a90c4dc60ce9287cd57b6cb02c04a3fb587bded1ac2`  
		Last Modified: Fri, 14 Feb 2025 21:07:19 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fd1ccdfddd0660fc3d2908d5a9919d6702f463a073cf54499e11ec9ed82764`  
		Last Modified: Fri, 14 Feb 2025 21:07:19 GMT  
		Size: 1.1 MB (1120319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01134ba51a71ecd085a0c6c6451bd05bec05415f073ecb4e54a77e98d5487480`  
		Last Modified: Fri, 14 Feb 2025 21:07:19 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7991eada79ae68e26230876ea45a3ae6b5459a92b5c0f7fe7f2c75595ed58b0`  
		Last Modified: Fri, 14 Feb 2025 21:07:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726d8d657943f9e970aa3537fe8992690920c21fe3af71d48c284d6769377f43`  
		Last Modified: Fri, 14 Feb 2025 21:07:25 GMT  
		Size: 102.1 MB (102145045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8001cdf901e0f58482b23b33500ee2d964277280534c391044d0954dfbcb71`  
		Last Modified: Fri, 14 Feb 2025 21:07:19 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504cbc948b8f5327a93c77c1e0eb131732a74dc04d1221355d34e94c9ad509f5`  
		Last Modified: Fri, 14 Feb 2025 21:07:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe9917edf464c90a4ca19cfbdee5f382c4651689fdd367a64072c689db739e2`  
		Last Modified: Fri, 14 Feb 2025 21:07:19 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aba31e2c080756acb28faf763f62ac18ba08d483a416169dee8e975c11f5ed`  
		Last Modified: Fri, 14 Feb 2025 21:07:19 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51de54b8a8bdbbfba611518ec998ad9b7273f3aef2f94bae0285b3d5ec26e99`  
		Last Modified: Fri, 14 Feb 2025 21:07:19 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:86954af99ee89a47013b25e00eeb8ac71d9b2272919d0f9b59c461a7ec618baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.9 KB (636939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc724ee38cf5bb0d6f4776d561ba3d55a3194b6b3b5051d98389fea69f34030b`

```dockerfile
```

-	Layers:
	-	`sha256:9524e6aad3a6f3c3287f4413efebb98fce1df147cfb9159bd633b67c0127e658`  
		Last Modified: Fri, 14 Feb 2025 21:07:23 GMT  
		Size: 592.1 KB (592111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700769085e8ef7c122124421e9046a15afc838986c458f5ceb0697906db2c082`  
		Last Modified: Fri, 14 Feb 2025 21:07:24 GMT  
		Size: 44.8 KB (44828 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:80d697b65eff643ab5c24ab925e0ce3559861e0c5964c0a907cb24ee970bd26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88920757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a200dfb3b8e91bbfd3e997ce15679f2a8b3536f80d0ff33a2f798c110d6a0e1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:01:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_MAJOR=13
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_VERSION=13.19
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_SHA256=482cce0a9f8d24c2447cfc7b2817e55f86d51afe5f7f1a85214bf93644e774ea
# Thu, 13 Feb 2025 18:01:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:01:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:01:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:01:24 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:01:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:01:24 GMT
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
	-	`sha256:8c90e9e047543c4cd91a154998c764996c396d165121b5da1c1e3c922107a60e`  
		Last Modified: Fri, 14 Feb 2025 03:08:09 GMT  
		Size: 84.5 MB (84454079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903dd30555dcea2eea79d908214d2248692794c5df0e38124b2843c50bb97fef`  
		Last Modified: Fri, 14 Feb 2025 03:08:04 GMT  
		Size: 9.0 KB (9017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417823a46c57b791cccf53f3852e83261612874026e94a2c6655187efb04528f`  
		Last Modified: Fri, 14 Feb 2025 03:08:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0409bbc3df483b5a6467c50fd56ed6f799b52659992fa28d9081dd4c3a33499a`  
		Last Modified: Fri, 14 Feb 2025 03:08:04 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8dc0ae5c9c18241c70bf036a7fec5ca9f10fc3653fc4e401116515eb44e499`  
		Last Modified: Fri, 14 Feb 2025 01:26:36 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df612d2391b1ecad069a50f620f1e36d8a142f5b9a8d82c59537ff63dcc56c8`  
		Last Modified: Fri, 14 Feb 2025 03:08:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:b77c8410a6d063424ba06aa0b2e8ddeafbe84d372402f15b2fb1e33abcb77068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 KB (44787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81edcc5040d9796bb8be73151b75d05a8f75198c8f8fb42520f6158ea068c2ad`

```dockerfile
```

-	Layers:
	-	`sha256:5e29f193254f7d4c19cb149c5cc00c695086eaad812955685fe608e5130d7e9d`  
		Last Modified: Fri, 14 Feb 2025 03:07:36 GMT  
		Size: 44.8 KB (44787 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:229edb30160cd0deaba12c3668966c82b444306b82540514f72b1f2c041a9526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (84044991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f957d6c4f3403209b06ba1cd07ef47725d137d66a1592f3486d676d3ad1a992d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:01:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_MAJOR=13
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_VERSION=13.19
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_SHA256=482cce0a9f8d24c2447cfc7b2817e55f86d51afe5f7f1a85214bf93644e774ea
# Thu, 13 Feb 2025 18:01:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:01:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:01:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:01:24 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:01:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:01:24 GMT
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
	-	`sha256:15c014f7c12dc79d36ea19b3427ade3e2a375f3c039e33073f1b4fa2977d8b9c`  
		Last Modified: Fri, 14 Feb 2025 03:52:47 GMT  
		Size: 79.8 MB (79845086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac6ab737cd6febfa4aeb26a2308d543edf924554b3242605a3281a6f66a6d9e`  
		Last Modified: Fri, 14 Feb 2025 03:52:41 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408dcaa952843553cc9ba673a8f34f221db71461f437a3c0256f2b894d925d6e`  
		Last Modified: Fri, 14 Feb 2025 03:52:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55160945647cc179d117a81132a1a8e40b70cf6e8fade646af767535189b5f7b`  
		Last Modified: Fri, 14 Feb 2025 03:52:42 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97610adb048beba4e6beb8586336a3eb735008badeabe03a72eba0b604a0c79`  
		Last Modified: Fri, 14 Feb 2025 03:52:43 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098876a7f4277592828373b51b018eb9fce55995af07bf5ba9d8b907dcb1e7bb`  
		Last Modified: Fri, 14 Feb 2025 03:52:43 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:8cf69e927635d7d2aeb780bfa91ce2c0a2bd7d03cad47e94e17d336d1d0be75c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.2 KB (638164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3997d314ecc4fa1ac2399dbfaf0dfd561949df23970ef2ddb73bdab08464946`

```dockerfile
```

-	Layers:
	-	`sha256:ac6cbed865590374ebfe5636bf75d3d0a9bcefc4c8502be7115855264d396b89`  
		Last Modified: Fri, 14 Feb 2025 03:07:37 GMT  
		Size: 593.2 KB (593162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dccd547bea84d76e0c4ea9746a8d24bb500a028d1374720f224a31c4d4d570ad`  
		Last Modified: Fri, 14 Feb 2025 03:07:38 GMT  
		Size: 45.0 KB (45002 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:8f3bbba2bdf911255bab2d3ea723964b28fbb81376016d5f44429fe1a1e4b82b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105851629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6543c1616e31216e53100429dbbd08cd48d735b3d45891b9689584ad53bee89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:01:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_MAJOR=13
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_VERSION=13.19
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_SHA256=482cce0a9f8d24c2447cfc7b2817e55f86d51afe5f7f1a85214bf93644e774ea
# Thu, 13 Feb 2025 18:01:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:01:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:01:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:01:24 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:01:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:01:24 GMT
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
	-	`sha256:3900a9c42326f20c92edc0f575f4997837f5b349df1c3fce69b1ce7bed09ac7d`  
		Last Modified: Thu, 13 Feb 2025 23:31:43 GMT  
		Size: 100.8 MB (100793033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7f41a454c14a465495c75f98690217916e013cb82f07e946eb7d6bfd63689f`  
		Last Modified: Thu, 13 Feb 2025 23:31:39 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27c37c021b77dd2576dfa324c83f93b2830e4477dfedebc54c56938301cb13c`  
		Last Modified: Thu, 13 Feb 2025 23:31:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f9f8d9b10cc410ab8d3325039dbc091d15a73909ae8057bc7d04abd019d7c0`  
		Last Modified: Thu, 13 Feb 2025 23:31:39 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f7f827ad6bca5a8db11c002717cb9097bd5cce430c1f4a9e45e0d611c99c86`  
		Last Modified: Thu, 13 Feb 2025 23:31:40 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48a39cc0a8931f0621e5d4a4d0e20e02e7ac6d4d7461cfb457c9aad9474b8c3`  
		Last Modified: Thu, 13 Feb 2025 23:31:40 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:09e3b0274567f00b77a5621512a631f951b0d17a6989765dce9ebb5894bf183f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.2 KB (638233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b00f638181124f0b96ab84ab92bae8041ffc23f872e7f35686678f59f6addd`

```dockerfile
```

-	Layers:
	-	`sha256:9d072d9134ac7b284c4d12ee5ce3ec175ab9e5a88d8de7e394896912c05e1da2`  
		Last Modified: Fri, 14 Feb 2025 00:07:55 GMT  
		Size: 593.2 KB (593182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39c3194cd751f079cdd6edb160f33854c0f1760275564bc67153afe5b55fc71c`  
		Last Modified: Fri, 14 Feb 2025 00:07:55 GMT  
		Size: 45.1 KB (45051 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; 386

```console
$ docker pull postgres@sha256:44c56017c7b6546f7ad1edbbffb9b0545c30645e02b15462c14f849597635d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115535850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed772d49156489506b453da6c8cf229664dc6ce565d8047804df9285678d27b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:01:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_MAJOR=13
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_VERSION=13.19
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_SHA256=482cce0a9f8d24c2447cfc7b2817e55f86d51afe5f7f1a85214bf93644e774ea
# Thu, 13 Feb 2025 18:01:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:01:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:01:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:01:24 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:01:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:01:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acfbfd9fcb2028f2d77277138146284ae556e811d7eef4b9f713a101e159f51`  
		Last Modified: Fri, 14 Feb 2025 00:11:50 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92264fd63faeab7f8c68f7cec02b741a84c4be24162d8ee5d904be5660a73d44`  
		Last Modified: Fri, 14 Feb 2025 00:11:50 GMT  
		Size: 1.1 MB (1095279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506bf0944f4458286a0b033959c9d34373a60dc3ef43ba020175311a54c0349d`  
		Last Modified: Fri, 14 Feb 2025 00:11:50 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afc97a73479fc2f325dd6d27115c8bc755b10affc0b70a97c66bc2390c5aab7`  
		Last Modified: Fri, 14 Feb 2025 00:11:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd69ab1e9c14b066e964539ea4512a346755b4bf886819efa03f08e698f8e398`  
		Last Modified: Fri, 14 Feb 2025 00:12:00 GMT  
		Size: 111.0 MB (110961264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fe7a728fb35b97b8c6ae79a83019c91b055aca353f553cc5d47124a5efd0d3`  
		Last Modified: Fri, 14 Feb 2025 00:11:50 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58eb202c034d02dc1e38ae1a781342e78260a5224899bcbb51df9c679940c8f`  
		Last Modified: Fri, 14 Feb 2025 00:11:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e7f43e9ee45aed2b5e1d5b5dbc8bd12be1051cca05193ae4bbd11b274dfe2f`  
		Last Modified: Fri, 14 Feb 2025 00:11:51 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1dda9475c8b3a421229330194591898fd0f4ea3b0bbaaa4a8c50ee15e49578`  
		Last Modified: Fri, 14 Feb 2025 00:11:51 GMT  
		Size: 5.4 KB (5413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c761f55a3248936888b18cbb6d7d804f196b67d7f2b36ef8226057b2126ce6`  
		Last Modified: Fri, 14 Feb 2025 00:11:51 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:118dfc7ae68d702eac9e304511e68b40cf3f279b080b3e1462a8e1b9e39b474e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.9 KB (637881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35483749e4ea87dd6473769e643ee955f1137e4fb914e579ac123e9aa855ff0b`

```dockerfile
```

-	Layers:
	-	`sha256:4dec852dd7d61e17cdc036c47a3b657f0df26cf8067430c6e53d89c8c43599fa`  
		Last Modified: Fri, 14 Feb 2025 00:07:57 GMT  
		Size: 593.1 KB (593101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cf3cfa3eea5edc74cae41d02475ca1bf5358051026b357717ba880505eedab6`  
		Last Modified: Fri, 14 Feb 2025 00:07:57 GMT  
		Size: 44.8 KB (44780 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:b2d25a309e46d0e91a986c050f62c5bd7989c0bc0dd76ed752317eef64c98428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93044556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0472178ef0257f14c6aa9a72215aa289ca64471a428fa8728414e56537f32d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:01:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_MAJOR=13
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_VERSION=13.19
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_SHA256=482cce0a9f8d24c2447cfc7b2817e55f86d51afe5f7f1a85214bf93644e774ea
# Thu, 13 Feb 2025 18:01:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:01:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:01:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:01:24 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:01:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:01:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e971de4eb277b3aa1b450ed7e2dd50144c9c0d0057e29a8f50797a51db3b050`  
		Last Modified: Fri, 14 Feb 2025 00:12:08 GMT  
		Size: 987.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b54f84ce7ed856da325479909312d14e436f584e61d6ad81c9e3ce62e8896d`  
		Last Modified: Fri, 14 Feb 2025 00:12:08 GMT  
		Size: 1.0 MB (1040366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace9e9faaf89a130786e2275383d3195fa28c6fc9af5e685039fb28e9135bafd`  
		Last Modified: Fri, 14 Feb 2025 00:12:08 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34f6ce65efb912d364eab57d91c19c17d0298a214302129f867d0138a9a3db3`  
		Last Modified: Fri, 14 Feb 2025 00:12:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b6e4f9b1ed1cf37db5d46398981415bf0ef8c32bd9e9ec653ee836ff13c9a3`  
		Last Modified: Fri, 14 Feb 2025 00:12:18 GMT  
		Size: 88.4 MB (88414398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cba8193554658abb4efc10f62212558e4ff8cee151b71f842ffc3b6f2c2906d`  
		Last Modified: Fri, 14 Feb 2025 00:12:10 GMT  
		Size: 9.0 KB (9016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d85fc3bff94f20623c189003290b7d9dd77c7b2390b7435ad514f86a8f8773`  
		Last Modified: Fri, 14 Feb 2025 00:12:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca8560c43f80ae888a6c2763e70c0dfc9930e65e707ecdb9c5d509c2ebe1c41`  
		Last Modified: Fri, 14 Feb 2025 00:12:11 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a5fc92b0f140d0cdf445d559b5cca8aa82a4a8b95fbb105eb975d40837ae76`  
		Last Modified: Fri, 14 Feb 2025 00:12:11 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344276e40dfeeb954f3a7a70ae7caf7ecf2e24761a8c53a9b505d11175eb0f99`  
		Last Modified: Fri, 14 Feb 2025 00:12:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:8dfe9e85ce1e9c078516ab1ba352e12e1cea7ddb57c0d9d2e57ab9a0463b637f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.4 KB (634428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7fd292330c370552afc611b9fd4995c5d2e427c34e0c4b3dfb5549c9e2ecd1`

```dockerfile
```

-	Layers:
	-	`sha256:b8806a03a9794e1c277a7ef3f513aff0ac4af154d529e2edbf90c46b1b73665f`  
		Last Modified: Fri, 14 Feb 2025 00:07:59 GMT  
		Size: 589.5 KB (589547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c937999caa7776c96d67e0578e92737a49d2e5cd77ce2af3d3961168a8f2aa6f`  
		Last Modified: Fri, 14 Feb 2025 00:07:59 GMT  
		Size: 44.9 KB (44881 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:5ea178626439df3fa22a948a7639bf3e9ff3a9389fe35d64a87a729067df2452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108726764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28520edf573b99991eaeaac27c79110179b59beeea5ed659e1f25d0464de9178`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:01:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_MAJOR=13
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_VERSION=13.19
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_SHA256=482cce0a9f8d24c2447cfc7b2817e55f86d51afe5f7f1a85214bf93644e774ea
# Thu, 13 Feb 2025 18:01:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:01:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:01:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:01:24 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:01:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:01:24 GMT
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
	-	`sha256:884a7b0a59407a8af3393f1222647292d302e0c1b62820ee53bb1ebd06bc095f`  
		Last Modified: Fri, 14 Feb 2025 13:06:12 GMT  
		Size: 104.3 MB (104270515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f38654af9c6eda92cdc20143fa6431351c0aaef078862a4f9d2a85b1f4efa3`  
		Last Modified: Fri, 14 Feb 2025 13:06:09 GMT  
		Size: 9.0 KB (9022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906e7ade68721789a862ccffa8e9da2112d69df37428885cc6052f44f2724de1`  
		Last Modified: Fri, 14 Feb 2025 13:06:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147d528fbe219f642b6347821e082abc23b53fc3d4c71a08e628443154d4d961`  
		Last Modified: Fri, 14 Feb 2025 13:06:09 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f897d7032cf0ce2e3e4237c2815cd57ef93e267eae34b54a7ca600a0745ec160`  
		Last Modified: Fri, 14 Feb 2025 06:22:29 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0eda752bddafbda72d76ee8f5f36c9be882877b96b8c4b39568bce763a3d73c`  
		Last Modified: Fri, 14 Feb 2025 13:06:10 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:b1fd93c2dd6b5339c92d59228d04922c2eb5ff59bc43158ded4dad25f5d53949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.1 KB (636093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6081f3623d47a3c95a6196e1f57c79a5b07f7289263ce329e09c89c83fda0d3b`

```dockerfile
```

-	Layers:
	-	`sha256:7d1126aed4ceb83b1b52f55a47a05d6dc32b98a545f3f438f79f73dff1f8ca2e`  
		Last Modified: Fri, 14 Feb 2025 09:07:28 GMT  
		Size: 591.2 KB (591205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cbac12f0ec8f88aaa22e0ecafa32d647581fe32ea95e19d26724a945b24acbd`  
		Last Modified: Fri, 14 Feb 2025 09:07:29 GMT  
		Size: 44.9 KB (44888 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:0a99eab1a090c87ae57c7afc30a06b0122f96e86fde5454dc0b77dd8550693b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117846149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc94149c875739f9c8d24def1b1d64f60e62386c1c09feddd15658f130a8da30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV LANG=en_US.utf8
# Thu, 13 Feb 2025 18:01:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_MAJOR=13
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_VERSION=13.19
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PG_SHA256=482cce0a9f8d24c2447cfc7b2817e55f86d51afe5f7f1a85214bf93644e774ea
# Thu, 13 Feb 2025 18:01:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Feb 2025 18:01:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Feb 2025 18:01:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Feb 2025 18:01:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 18:01:24 GMT
STOPSIGNAL SIGINT
# Thu, 13 Feb 2025 18:01:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Feb 2025 18:01:24 GMT
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
	-	`sha256:67788e83a37eb9ceb4ed218e175964735447267a80a965c32a76b2ed0aedf235`  
		Last Modified: Fri, 14 Feb 2025 05:06:07 GMT  
		Size: 113.3 MB (113278524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4091abf875b356bf13d9eb326b8821cf67ea88cce5d60bbf141c1a6d056ee5e`  
		Last Modified: Fri, 14 Feb 2025 05:06:08 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20e2ec0d6f24a8d5600377551634a751c023f9e49a465574e8eff07e404b90f`  
		Last Modified: Fri, 14 Feb 2025 05:06:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e8a806ca25d935fd8f4fc8dfb76d7f6bf0c25b1629c19b64b7c58af7a0086b`  
		Last Modified: Fri, 14 Feb 2025 05:06:10 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ece1d16e579e7550f1676e655561198923a87c3035d7056a804db31f980bbe`  
		Last Modified: Fri, 14 Feb 2025 05:06:10 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a490b25475aab0e483ea27a0dcde424182268fc249169590d59772d689e6db0`  
		Last Modified: Fri, 14 Feb 2025 05:06:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:318295a1b218a628e591a7e9a879967628be206e3ddf61359c89fc72bc58e170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 KB (636003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d78388b75811c659e4ce7762f38631301405163dc3589475140715fd5ac11a1`

```dockerfile
```

-	Layers:
	-	`sha256:27d48df43fb754fae8055103e0d571505b51cbe5d1b7ccdc60ba26e1b64d8361`  
		Last Modified: Fri, 14 Feb 2025 03:07:45 GMT  
		Size: 591.2 KB (591175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d48df0c6076d6eaa511581c799d5e18a45c1f25fde17f7946cc9982bd1faea07`  
		Last Modified: Fri, 14 Feb 2025 03:07:45 GMT  
		Size: 44.8 KB (44828 bytes)  
		MIME: application/vnd.in-toto+json
