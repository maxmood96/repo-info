## `postgres:alpine3.21`

```console
$ docker pull postgres@sha256:741cad88af2b5501ab3cc7aa4e834e50647dabc5af57b5297c9e480b99f3ab43
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

### `postgres:alpine3.21` - linux; amd64

```console
$ docker pull postgres@sha256:15f2fd73d9d46770d2410e581210bf7c19dadbb3450194e7f5908b5e99185ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110783095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca30e05eaa0e67d6af4b9372401a8d7f74b451d6e9482be47c287bfd46d44763`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV LANG=en_US.utf8
# Fri, 30 May 2025 21:09:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_MAJOR=17
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_VERSION=17.5
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_SHA256=fcb7ab38e23b264d1902cb25e6adafb4525a6ebcbd015434aeef9eda80f528d8
# Fri, 30 May 2025 21:09:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 30 May 2025 21:09:41 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 30 May 2025 21:09:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 21:09:41 GMT
STOPSIGNAL SIGINT
# Fri, 30 May 2025 21:09:41 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 30 May 2025 21:09:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7034244a914a565627fd2b2145f4299ee63b6736342c2ba0bcf40a3452983b`  
		Last Modified: Tue, 03 Jun 2025 13:31:14 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8016e6109e974641fc795e47543246c85999e7c858a263e59895929c4462ad14`  
		Last Modified: Tue, 03 Jun 2025 13:31:14 GMT  
		Size: 1.1 MB (1120321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e5a9a905b92615226ae6a0042f5838652e75044899dbd48ebc7d9a2835dd39`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdbdfb8dadd15f27f1569ed104de104055b7565bc4b6aeb6d3e0753046d2f96`  
		Last Modified: Tue, 03 Jun 2025 13:31:19 GMT  
		Size: 106.0 MB (106003599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fa882872daff37ba13fccf2493c8e71c6d0e6130e8b585fba33ce293b9106f`  
		Last Modified: Tue, 03 Jun 2025 13:31:15 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554d49d0d0337a0a5b9cfabb4761dab604df68c142d9df5a17a5d15d4b6cffcd`  
		Last Modified: Tue, 03 Jun 2025 13:31:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d182e82c312b73c4dc3d14c9a226e3cbc8757c33f681b1539e8f100b1ee1a7`  
		Last Modified: Tue, 03 Jun 2025 13:31:16 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc3843dc9db393ea077072c021b2d0b3ac3cf004eeb4cebc44f2d6e8fea17e6`  
		Last Modified: Tue, 03 Jun 2025 13:31:16 GMT  
		Size: 5.5 KB (5471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819418ed6813093e79fd6588a077635a2c4159d8e7be6e59f2daaada26264dd1`  
		Last Modified: Tue, 03 Jun 2025 13:31:17 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:d6369ad11b5fd4f179fdeca025215bfb3b5022ef76ed1b320d5cce0cc7e1cbff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.4 KB (640357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb17b9464a368832fc2ea34e7fbe538a2e726eb28f83e750522029d5acfbde0b`

```dockerfile
```

-	Layers:
	-	`sha256:1f709a5f8ce957f0269087fb6ab36800e4d3b96da72f5bbc9960c9df3a0333fc`  
		Last Modified: Mon, 02 Jun 2025 17:31:38 GMT  
		Size: 599.0 KB (599006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc55d14504ff1a76e3b100a23b6bba8806010b827a12734ad89291ca33f95135`  
		Last Modified: Mon, 02 Jun 2025 17:31:38 GMT  
		Size: 41.4 KB (41351 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.21` - linux; arm variant v6

```console
$ docker pull postgres@sha256:61c8cfd8a9d4241016f794ba1120c44bb5f751a98ea74787d55557da60d2329d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90316486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2173abeae7b01dfee100377eb901786451040ac0c6649be85e8d8a35b398f012`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV LANG=en_US.utf8
# Fri, 30 May 2025 21:09:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_MAJOR=17
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_VERSION=17.5
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_SHA256=fcb7ab38e23b264d1902cb25e6adafb4525a6ebcbd015434aeef9eda80f528d8
# Fri, 30 May 2025 21:09:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 30 May 2025 21:09:41 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 30 May 2025 21:09:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 21:09:41 GMT
STOPSIGNAL SIGINT
# Fri, 30 May 2025 21:09:41 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 30 May 2025 21:09:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e8cc19bee9308afcbf52843a00e4ef4972c49cf21acd9b92368cecf528ff49`  
		Last Modified: Sat, 15 Feb 2025 00:09:03 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781627176b8f9e10a830d9e3a634776cd0db6531992b444881c58b767652e146`  
		Last Modified: Sat, 15 Feb 2025 00:09:03 GMT  
		Size: 1.1 MB (1086598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d02770e2c9e59d06a2bd5c652ffcad00b9acafe2e323aff7bd4c2aed933707`  
		Last Modified: Sat, 15 Feb 2025 00:12:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8505f014824815623f83765e872798ded7519194ed6b46c2657aedb6ab27f764`  
		Last Modified: Mon, 02 Jun 2025 17:33:29 GMT  
		Size: 85.8 MB (85848227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a066cef7d1e79e9f02630544a640d00906c9dff09a8f326fef9567be6f0a3f0`  
		Last Modified: Tue, 03 Jun 2025 15:17:23 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d3cafd86e3a40ac345803fad0d645df11d62b2d21bc2987c812d9da989e80c`  
		Last Modified: Tue, 03 Jun 2025 15:34:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d3a3a6d9f2f4e5b73d67b2c78ac90bb20f0d12d9a8e718db8d0303cbdfa4d5`  
		Last Modified: Tue, 03 Jun 2025 15:38:52 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47e91585e5a9134a8d73393a1f9aebdc21f0349221e4a8970a4de0e036bc1bd`  
		Last Modified: Tue, 03 Jun 2025 15:28:28 GMT  
		Size: 5.5 KB (5476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a58fa29018bd7d3066811850a6a1582564081c72a6575507c80b4f3fcdb0234`  
		Last Modified: Tue, 03 Jun 2025 15:30:15 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:eb5443a0e5393c98df1a8601e9508a1372ca9346b91f13fdec95c5608f34b127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec28a1f97264150af7534600612d4804a2d439334ec1d0921923ee79b7d0b02`

```dockerfile
```

-	Layers:
	-	`sha256:eae3b198bc58e0fcfe7c836eb37339259a37bcde3f28237bb4d88f4317252590`  
		Last Modified: Mon, 02 Jun 2025 17:33:26 GMT  
		Size: 41.3 KB (41289 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.21` - linux; arm variant v7

```console
$ docker pull postgres@sha256:9d83892b325a455b44c144a996be3156c1475abcb986a154708644731706bf4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85502701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5a86b48e673aeee4756965d43e0ff7d29c39f518b890813a60cc37fc69b152`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV LANG=en_US.utf8
# Fri, 30 May 2025 21:09:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_MAJOR=17
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_VERSION=17.5
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_SHA256=fcb7ab38e23b264d1902cb25e6adafb4525a6ebcbd015434aeef9eda80f528d8
# Fri, 30 May 2025 21:09:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 30 May 2025 21:09:41 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 30 May 2025 21:09:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 21:09:41 GMT
STOPSIGNAL SIGINT
# Fri, 30 May 2025 21:09:41 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 30 May 2025 21:09:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ada47321bd0e89157bae4052aa7de0b68f59e22e5aa8ed76cb27a9a4fb2758b`  
		Last Modified: Thu, 08 May 2025 19:52:10 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997421b050761e5bc8fffaa3538a99a0dfde2e21a4b3c0d5f0432f97e3b5127d`  
		Last Modified: Thu, 08 May 2025 19:52:12 GMT  
		Size: 1.1 MB (1086588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2254c9bfb60716e855593990632ba5474ac42c7a065d45aa04f922b0ee39f083`  
		Last Modified: Thu, 08 May 2025 19:52:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1721ac7a4178a855ef732bff747545d7942da4ec95f6795d4643df632e675fe`  
		Last Modified: Thu, 08 May 2025 20:20:43 GMT  
		Size: 81.3 MB (81301049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a803adc1dcc5b57b0fc1ef7afb9688f6e8e995100b706b38e03920a63dd2fab`  
		Last Modified: Thu, 08 May 2025 19:52:12 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3d0d2200f7d8b90fc7ee909aadefd6a304a49c2dfdb3db5121bde300ecf6ba`  
		Last Modified: Tue, 03 Jun 2025 15:41:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5288c80923937cdf9f64e701656e690c6ea7d247022138ac1e1461cdcb1241b5`  
		Last Modified: Tue, 03 Jun 2025 15:29:16 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112dd2093ad8862f8a110ff0eeef8a968de06f9320a874b5e62581dc6f1f6c27`  
		Last Modified: Tue, 03 Jun 2025 15:11:08 GMT  
		Size: 5.5 KB (5478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b1cb18cf3cc23f8ff064b9fe15ac968bcab1e50d8955bab985ab3d0bf207ec`  
		Last Modified: Tue, 03 Jun 2025 15:30:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:3b64c4e41d1a0dfe488f83f09dddf1984d971300b17419b2aa7aa8c786643e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.5 KB (640538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463517b9eaae4fccc9b1f6ac53884c21a30ecb5549338c69cfaaea6daecf52a8`

```dockerfile
```

-	Layers:
	-	`sha256:d5b316fb34e31e270f56ec0eaf2e58ff7c6501d311ee8a1093acbc16e281934e`  
		Last Modified: Mon, 02 Jun 2025 17:49:43 GMT  
		Size: 599.0 KB (599034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c10b3af2b2ef5f689e22afd6961aa52d0d188fe90b24e1c1287738da01e969ec`  
		Last Modified: Mon, 02 Jun 2025 17:49:43 GMT  
		Size: 41.5 KB (41504 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:66d4adb4d17f8add77c99d6da0cce6a52579c290f93fa2d44bcdd5b8bc1fe5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106659530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6bc25b63ef4a078cbcc23c9dee6775f1ca5bae9356aac0d80719839a9aac37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV LANG=en_US.utf8
# Fri, 30 May 2025 21:09:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_MAJOR=17
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_VERSION=17.5
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_SHA256=fcb7ab38e23b264d1902cb25e6adafb4525a6ebcbd015434aeef9eda80f528d8
# Fri, 30 May 2025 21:09:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 30 May 2025 21:09:41 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 30 May 2025 21:09:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 21:09:41 GMT
STOPSIGNAL SIGINT
# Fri, 30 May 2025 21:09:41 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 30 May 2025 21:09:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d03f0f2d53b2dbd9eb483b0627ccff77722b5cd779ea77b53d0c300329320e0`  
		Last Modified: Tue, 03 Jun 2025 13:33:42 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7253dfc6422805ac3c15fda3414a5e3fb679f89df5a9ecfb3b80db788b4e8dcf`  
		Last Modified: Tue, 03 Jun 2025 13:33:43 GMT  
		Size: 1.1 MB (1050058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b90ea9249963dcb9805814c17104a6f70dae2a0e479b6dcf41d3ab2ee8137ac`  
		Last Modified: Tue, 03 Jun 2025 13:36:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b12df9c2f717b96a1fefd7907e926736c68ebf8d2f945a0c7993c469bb3a3f8`  
		Last Modified: Tue, 03 Jun 2025 13:37:03 GMT  
		Size: 101.6 MB (101599513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7859132f9241c4258602910a6991386a06cf195ce8078a53551cc31e6dce7791`  
		Last Modified: Tue, 03 Jun 2025 13:36:45 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dedbe20ee2a91028d2b5470656a2c5af612c0f6b25036d9c7646fa37a63899`  
		Last Modified: Tue, 03 Jun 2025 13:36:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345193ef5d94e4f916b9fcb2797ef15bf5a17a471977efcf2360cc7f10471a20`  
		Last Modified: Tue, 03 Jun 2025 13:36:45 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b99eb699b4d105986b598d2159657c72133b7d727e3d0799bb4b3fa4cea2a4`  
		Last Modified: Tue, 03 Jun 2025 13:36:44 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365659e7fdb5b5e2daa6e2aa18812a55636160c337610079cab7122443b9645c`  
		Last Modified: Tue, 03 Jun 2025 13:36:46 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:80d9beee90d08872b89ca9939560c8f511c7ed7f8545c48184a884dc3fc6e74c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.6 KB (640598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b978199db3b400e9f9d237e47035e46849b75194ff9216bdb439d4482eb16fbc`

```dockerfile
```

-	Layers:
	-	`sha256:40522f4ba36ff1d6196a9d57bcf692f9df55d3ca9066a19662cc2c7c85924552`  
		Last Modified: Mon, 02 Jun 2025 17:53:27 GMT  
		Size: 599.0 KB (599050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ce87829130d523a57d73656022e044fbae871e8702ddfd7396ad614a280389`  
		Last Modified: Mon, 02 Jun 2025 17:53:27 GMT  
		Size: 41.5 KB (41548 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.21` - linux; 386

```console
$ docker pull postgres@sha256:dd4421f0bcd3da10ac19cb2d00859a941935cf3a5b619f3f5e5f5d4ba1eb073d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116966006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d013adc2372180b9bfbd2662efe862368b3030408db3d1122cdd873a3898744e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV LANG=en_US.utf8
# Fri, 30 May 2025 21:09:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_MAJOR=17
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_VERSION=17.5
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_SHA256=fcb7ab38e23b264d1902cb25e6adafb4525a6ebcbd015434aeef9eda80f528d8
# Fri, 30 May 2025 21:09:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 30 May 2025 21:09:41 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 30 May 2025 21:09:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 21:09:41 GMT
STOPSIGNAL SIGINT
# Fri, 30 May 2025 21:09:41 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 30 May 2025 21:09:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8a1dccd2ef048f4f2b7abba55bbbe4c43e009403b8e78fc16462ad9b4615de`  
		Last Modified: Tue, 03 Jun 2025 15:24:51 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf78b146db4020caede9287bf395e4b08d01cf092ccb3298a8c59f4fcae7570`  
		Last Modified: Tue, 03 Jun 2025 15:33:56 GMT  
		Size: 1.1 MB (1095260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fce53630f2d89af763b1aa9c3c63739ec9fb7de523b504d0ec79143f743c806`  
		Last Modified: Tue, 03 Jun 2025 15:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47993a8479688246c2c844ca6ede4847adb03928b4a80790bb1d218df4509d8c`  
		Last Modified: Mon, 02 Jun 2025 17:32:43 GMT  
		Size: 112.4 MB (112390195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83290deb1de87b37d6ebcc26cf1f74d9a874afc05fa3e62f4d4abc0f4769a48`  
		Last Modified: Tue, 03 Jun 2025 15:19:29 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6785a35dbb9f3ac8f66c71d7e527adab31b86a60e4083a0cdf3bf0ae7ebf98e9`  
		Last Modified: Tue, 03 Jun 2025 15:11:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759f3a007e369490b9be4ed6d92b5106050abf5f3984bf7dc4698a8a7045e526`  
		Last Modified: Tue, 03 Jun 2025 15:37:28 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ef1c977d0be5a058a9490bd147ad24772f8c0b5ad3b67560716cfe344a9a81`  
		Last Modified: Tue, 03 Jun 2025 15:30:39 GMT  
		Size: 5.5 KB (5476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a301bb586f196aa66bb34520a6ff9b9ed7a5628ac9e4ce93269a67055b00ac`  
		Last Modified: Tue, 03 Jun 2025 15:11:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:9d54ef40e70231da50cd65451a619436f2b470408b4bc05e23ebccf6b0838bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.3 KB (640296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355f10f33e118d86b7d26762000cde7de18884cda5194760fd0d43608a25f1df`

```dockerfile
```

-	Layers:
	-	`sha256:611dcc452f6840599c2b88c4fa92bb61db0d5944e37a29765d0703ff8acd1e39`  
		Last Modified: Mon, 02 Jun 2025 17:32:40 GMT  
		Size: 599.0 KB (598986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1f940649feda76e4e766781acfd4729d30e7984bba9028281e421094b929018`  
		Last Modified: Mon, 02 Jun 2025 17:32:40 GMT  
		Size: 41.3 KB (41310 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.21` - linux; ppc64le

```console
$ docker pull postgres@sha256:3652a0864506e845baf484fb2ec29ab736d33885a654f0df7381b3a63f6df803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94589474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78477d813b6e97c19e3de51d8023b84c33021c4939911c18ebb90e43d05f60d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV LANG=en_US.utf8
# Fri, 30 May 2025 21:09:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_MAJOR=17
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_VERSION=17.5
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_SHA256=fcb7ab38e23b264d1902cb25e6adafb4525a6ebcbd015434aeef9eda80f528d8
# Fri, 30 May 2025 21:09:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 30 May 2025 21:09:41 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 30 May 2025 21:09:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 21:09:41 GMT
STOPSIGNAL SIGINT
# Fri, 30 May 2025 21:09:41 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 30 May 2025 21:09:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bbfa9887a7a761f236c6a62f7e2b1f9e06e4c49edc5445a1383c30a024f0fe`  
		Last Modified: Tue, 03 Jun 2025 15:33:09 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9154ad7d6d2b8215d6e5c17c7126973ef555179af7445e48dd15afbc769dab`  
		Last Modified: Tue, 03 Jun 2025 15:36:41 GMT  
		Size: 1.0 MB (1040368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c56f5d252071b2e877b4f26c00365864af80a4943ec96ccd1dbec988c86c19`  
		Last Modified: Tue, 03 Jun 2025 15:24:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422913e99c73bb8a9d16ae59e314eff244da153e66b92a1ddbe9bc934ec7a99e`  
		Last Modified: Mon, 02 Jun 2025 17:42:13 GMT  
		Size: 90.0 MB (89957833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2cfdaba499b06989db1586273750245ca4620627bfb5fcd00bdeecb3e74e48`  
		Last Modified: Tue, 03 Jun 2025 15:42:23 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd1260bd2971d85c4ec0c08959b03a3ca6858f63c5808d346c45111648234a2`  
		Last Modified: Tue, 03 Jun 2025 15:25:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1198de132a983e605843b2ce6e7976852e9b43f8963704c313058d7aee234caa`  
		Last Modified: Tue, 03 Jun 2025 15:18:18 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7cc00bfcd4d6acd86df5dde9b814a09d142f78b7817218ca5c1d81c55b1aae`  
		Last Modified: Tue, 03 Jun 2025 15:35:11 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6042945100ced5108b80e2b1327550863c6730ebfe90bd70e50edeb9e283576`  
		Last Modified: Tue, 03 Jun 2025 15:35:13 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:d1d7edaefd458cbc11df5dca55ba83a50cfeed2a9a4a5cc0a155aedfb1e9bc30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.8 KB (636818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4271108cc713a404a3cb8c2ee44f65f59355f0e1bf979c466c3e50e736617c6`

```dockerfile
```

-	Layers:
	-	`sha256:b3c9572fc733dce4007df12e9bf0193918e66507ad14f63b3e9fb9a1cb1f2068`  
		Last Modified: Mon, 02 Jun 2025 17:42:10 GMT  
		Size: 595.4 KB (595421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:823c47f5a22b6d087c2e36bb47ba1f0f179929ace873b654d94cfa2bb0d13365`  
		Last Modified: Mon, 02 Jun 2025 17:42:10 GMT  
		Size: 41.4 KB (41397 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.21` - linux; riscv64

```console
$ docker pull postgres@sha256:b47a8d921537ebfa6a0212f8a84b9a643e1094daa7f2190312a851273bfa9f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110903063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2650e42c26a7b29170fcb666e336df081f5973e49f47fcaba774284cb8bc9bcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV LANG=en_US.utf8
# Fri, 30 May 2025 21:09:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_MAJOR=17
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_VERSION=17.5
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_SHA256=fcb7ab38e23b264d1902cb25e6adafb4525a6ebcbd015434aeef9eda80f528d8
# Fri, 30 May 2025 21:09:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 30 May 2025 21:09:41 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 30 May 2025 21:09:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 21:09:41 GMT
STOPSIGNAL SIGINT
# Fri, 30 May 2025 21:09:41 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 30 May 2025 21:09:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51c32376219c4b96f02563de145a6dae5a45bd7698b8c7ca6f6da052086070b`  
		Last Modified: Fri, 09 May 2025 07:05:16 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8288dcf7d76e423837c7b22aaeabb3ffce916e0d4021374ef1030da4496878fb`  
		Last Modified: Fri, 09 May 2025 07:05:15 GMT  
		Size: 1.1 MB (1089773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5a6054c02a12ecf16737cbca62821e6155ebdde1b28847ca415fd5ea3a92df`  
		Last Modified: Fri, 09 May 2025 08:11:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a478cd1a774b2f9789297dfef6745280ce131817c318f28f529cec47ed668cd6`  
		Last Modified: Fri, 09 May 2025 07:05:31 GMT  
		Size: 106.4 MB (106444904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7272236851d12827d72d27b02831de024c21a906b4e455e053bc355ba01e1e38`  
		Last Modified: Fri, 09 May 2025 07:05:16 GMT  
		Size: 9.9 KB (9887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d600d6a4bc250fcb8ba11b1f05ebbbf25d3e9d67d5f06e94b0c51ccaa67ebd`  
		Last Modified: Fri, 09 May 2025 07:05:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac81c2a0370edc7d9f68782fc583e06350671f1554cbda9f9ef00c029d7b36c`  
		Last Modified: Mon, 02 Jun 2025 18:57:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef1310fbfd53ad6ea4db305d76b46e81ec299dc8bed35565bcb3131ffd96814`  
		Last Modified: Mon, 02 Jun 2025 18:57:48 GMT  
		Size: 5.5 KB (5480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f10484f7dc8ab1b9664f79b6a6e7b5681d03705586bae598c876ab0d9db0d`  
		Last Modified: Mon, 02 Jun 2025 18:57:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:c07f86a22317accab6ddfb54f88cdc9fd7108ee372be61300f9e902a7b7d3dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.5 KB (638482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d551607a161adb5ceaf57c535e1c1be715c0a2f200d921f48a9a3d6e95cfe68`

```dockerfile
```

-	Layers:
	-	`sha256:c4ce3886c53b3be97291453dea18f1ef4f28f4cf331106b9c606644184817a26`  
		Last Modified: Mon, 02 Jun 2025 18:57:48 GMT  
		Size: 597.1 KB (597079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1fe183725e45ab1b45e9df51ff3dc96ed9c6521cab08da1ab81d9800e097227`  
		Last Modified: Mon, 02 Jun 2025 18:57:48 GMT  
		Size: 41.4 KB (41403 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.21` - linux; s390x

```console
$ docker pull postgres@sha256:58ee20fea810be0a20cb36a7121e832c45ded2439b67629c24c189ea17598afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119387308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c25df6a1d0077bd35bc52aad86effae722a9fd492108a6db6e1d3e3d35e422`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV GOSU_VERSION=1.17
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV LANG=en_US.utf8
# Fri, 30 May 2025 21:09:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_MAJOR=17
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_VERSION=17.5
# Fri, 30 May 2025 21:09:41 GMT
ENV PG_SHA256=fcb7ab38e23b264d1902cb25e6adafb4525a6ebcbd015434aeef9eda80f528d8
# Fri, 30 May 2025 21:09:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 30 May 2025 21:09:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 30 May 2025 21:09:41 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 30 May 2025 21:09:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 21:09:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 30 May 2025 21:09:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 21:09:41 GMT
STOPSIGNAL SIGINT
# Fri, 30 May 2025 21:09:41 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 30 May 2025 21:09:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca41bc03c66f2db51ee7ccecf095cd1dba41a34a6d831663f4096bc1e32f4c79`  
		Last Modified: Mon, 02 Jun 2025 18:33:04 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e901e5ec0b869a1daf11fbf0499629c10c3fa04e7ffc3eb1336b6cb3d9dbb45`  
		Last Modified: Mon, 02 Jun 2025 18:33:04 GMT  
		Size: 1.1 MB (1084558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5742612fbc0f15f69ffd8bc6e5b145c445d9dd349c510e6aa97555bbaa4dda`  
		Last Modified: Tue, 03 Jun 2025 13:50:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3d316c82801c2c26b000694f7f6aef9413691d9fdf4751a7a002ed71cefe4f`  
		Last Modified: Mon, 02 Jun 2025 18:33:07 GMT  
		Size: 114.8 MB (114818250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636900436b96c0ed6e28a5093a807f8048d34fb6de9ed8b95a299f48c8fcc989`  
		Last Modified: Tue, 03 Jun 2025 13:51:55 GMT  
		Size: 9.9 KB (9888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ad786dac001bc35250671ca1b3525dcdf2224543f52ad10dcc81c456433aad`  
		Last Modified: Tue, 03 Jun 2025 14:23:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d19cc0902761a8ab1b263aa2e7a8414765ac90aaf75ac9de5fb93c470809b1`  
		Last Modified: Tue, 03 Jun 2025 13:40:01 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df4135a9e75a2198f51def7797b7fe6902a3c9ae52beb9baea60f0d40b2b6e9`  
		Last Modified: Tue, 03 Jun 2025 13:50:23 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74142e2ac13c1f7e2bf399b2917e01aa023420d95345ea179c402e03b97bb286`  
		Last Modified: Tue, 03 Jun 2025 14:09:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:e8132f375ca5a3627c67baf83f6652b1ca8f78ba689cc1a78b21e6eb6123f070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.4 KB (638406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cedc0a1ebd8355b644d4f443a2947b363c5505167e7932fab4cc7b4e0c09ca6f`

```dockerfile
```

-	Layers:
	-	`sha256:4f649fb15db0b7071bec1b827f7c70f2425a33e5aa4cf43968faca655528fb9c`  
		Last Modified: Mon, 02 Jun 2025 18:33:04 GMT  
		Size: 597.1 KB (597055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aba4a658afac9bd2d21829e99df62dfd46790b43a73afd559a544ff8ab705bb`  
		Last Modified: Mon, 02 Jun 2025 18:33:04 GMT  
		Size: 41.4 KB (41351 bytes)  
		MIME: application/vnd.in-toto+json
