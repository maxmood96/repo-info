## `postgres:19beta1-alpine3.23`

```console
$ docker pull postgres@sha256:86c758623a2f1db2c1e34d0651c296647de30529ffd751512ac5fc25b2c87d40
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
$ docker pull postgres@sha256:fd6ab0b29f59782942125d5907443d2bffb9996bc5f5b90358ca574ca6fae637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123274010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ce9d9cb7ea07027a89dab3f29db63f7d0f3745ca1ca35e6b30b576b64d823e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:57:30 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:57:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:57:30 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:57:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:57:30 GMT
ENV PG_MAJOR=19
# Tue, 16 Jun 2026 22:57:30 GMT
ENV PG_VERSION=19beta1
# Tue, 16 Jun 2026 22:57:30 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Tue, 16 Jun 2026 22:57:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:04 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:04 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Tue, 16 Jun 2026 23:00:04 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:04 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:04 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:04 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:04 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f50f8b241b18d1bed646fcf5fd1a513aedb95b5ea278aa0270aceab1491bdf`  
		Last Modified: Tue, 16 Jun 2026 23:00:22 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675ed19fc8127094c444463b79b9882e7755e4fdf9908f90c2d99c27370bb14`  
		Last Modified: Tue, 16 Jun 2026 23:00:22 GMT  
		Size: 919.1 KB (919055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d452e19bc168c2653e01ba8e38feee061a7a86e28a793fdfdc51e78c487acd`  
		Last Modified: Tue, 16 Jun 2026 23:00:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cb50da96b38561a0e9fe44c0656cf124076de7493b5f681be5af4a985188a1`  
		Last Modified: Tue, 16 Jun 2026 23:00:25 GMT  
		Size: 118.5 MB (118462257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55741dd7c3a5903efdb2db7192e94ba3ada9ddce02fe15805326889c162ee17b`  
		Last Modified: Tue, 16 Jun 2026 23:00:24 GMT  
		Size: 21.0 KB (21012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ed40f595e1f51b4ef776c2b77e4339724ba23b3973ad31cbfc5edc715be465`  
		Last Modified: Tue, 16 Jun 2026 23:00:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1da7bd61e06ad5cae92086f123629e5bc38906307a4f7b82c1487bb17cb0792`  
		Last Modified: Tue, 16 Jun 2026 23:00:25 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e96f9d309e4746bee4b39e9f97c3b493e075aefd1ea85816ec792a4f640b642`  
		Last Modified: Tue, 16 Jun 2026 23:00:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:94cd99f86f549a5967867abd8efba585b7f170dc992b310cadc4c391e368669a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.3 KB (655290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0347649f1e315699767c3dba0b6d352d2c1c8ff6d4ee5fa2f0dcfaba3162897e`

```dockerfile
```

-	Layers:
	-	`sha256:9128dc2b63722bffed95c012f1ddf624d5ad9d03a968e815cacb2e80b2cb78ed`  
		Last Modified: Tue, 16 Jun 2026 23:00:22 GMT  
		Size: 615.8 KB (615768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1402dfe3e017dd71f6d347aecb1167881b164f4ddea3ff6f072824a2b79c6a71`  
		Last Modified: Tue, 16 Jun 2026 23:00:21 GMT  
		Size: 39.5 KB (39522 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.23` - linux; arm variant v6

```console
$ docker pull postgres@sha256:ee32c2d5961f31a7d2db034b45ab0e37da676a8caec6f32378da8ef3760de68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119117114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4827639a22caa5cd8dd9e6108ee375e00fccbe086156dd4445628cf6f5c08e58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:43 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:57:47 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:57:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:57:47 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:57:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:57:47 GMT
ENV PG_MAJOR=19
# Tue, 16 Jun 2026 22:57:47 GMT
ENV PG_VERSION=19beta1
# Tue, 16 Jun 2026 22:57:47 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Tue, 16 Jun 2026 22:57:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:47 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Tue, 16 Jun 2026 23:00:47 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:48 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:48 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2297af6cac3928555a9c0076cb670a7e572be6f216abe0b3b65e9de83b55a17`  
		Last Modified: Tue, 16 Jun 2026 23:01:04 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9386da7fc45eeba3fb5776b41d9539e14f7b9c0b20f616c59e52101e33d70d8`  
		Last Modified: Tue, 16 Jun 2026 23:01:02 GMT  
		Size: 887.1 KB (887118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f711abd8ada553fa5fd361d86d74c12a5f79c5290b7a47d36a9daeb7ff3c866`  
		Last Modified: Tue, 16 Jun 2026 23:01:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcf6de37dc9051e0e79ebe9b299085f235e7298c448aef1fa3a2185552b8ca9`  
		Last Modified: Tue, 16 Jun 2026 23:01:06 GMT  
		Size: 114.6 MB (114629634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e958bab93ec3fcbf32734268b47110a518232d6103c9262c0b6b0e1c34d7fe6c`  
		Last Modified: Tue, 16 Jun 2026 23:01:03 GMT  
		Size: 21.0 KB (21004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2396c3d3aad325f860d840e5b742cfcad0bce25369a13641a2f0c8b567a2941`  
		Last Modified: Tue, 16 Jun 2026 23:01:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06414ecaf4a02441c614177f9f75db6bc2007c73caaa260711e03c4ad4a1f1e`  
		Last Modified: Tue, 16 Jun 2026 23:01:04 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcf0feb00894476c50ea26ffc0f810ffae1ef43436bc95713112bf9b5e25653`  
		Last Modified: Tue, 16 Jun 2026 23:01:06 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:71c8170ae96d0ebe9afa52309dbb18c80c9d48275aa0814c08fd79cefe98b6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 KB (39441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8981016658eb82be0abdaa8f6d8f8a8b531dc78b17281c42bd1de18b61b4bfff`

```dockerfile
```

-	Layers:
	-	`sha256:9ac740c00d50e0efc59f58b2d2eb810d5a8af51a7defe99684bffb684f337094`  
		Last Modified: Tue, 16 Jun 2026 23:01:02 GMT  
		Size: 39.4 KB (39441 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.23` - linux; arm variant v7

```console
$ docker pull postgres@sha256:54b0ecda585d4bf5e09cf780d92ff3ebcd00bf65b30846ecf085b2c4ea2cca76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112493376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048820f4f02e0a8005b46a7f5e00c5adfd78708ba371964134da248aed548853`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:57:11 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:57:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:57:11 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:57:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:57:12 GMT
ENV PG_MAJOR=19
# Tue, 16 Jun 2026 22:57:12 GMT
ENV PG_VERSION=19beta1
# Tue, 16 Jun 2026 22:57:12 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Tue, 16 Jun 2026 22:57:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:05 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Tue, 16 Jun 2026 23:00:05 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:06 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a9f2578f3c98424e1ab050f20c2f0ba3d1850009c3bada92e7e7a74a4d6b6c`  
		Last Modified: Tue, 16 Jun 2026 23:00:20 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de11f0e05cf97ab69cbfe8c2402f5eeb63131a304ec0869b6068e89af388fb69`  
		Last Modified: Tue, 16 Jun 2026 23:00:21 GMT  
		Size: 887.1 KB (887124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682509fd64731ef6d07bbad90f2132657e2ee4d9f64095c3cc6601f0bc3d874b`  
		Last Modified: Tue, 16 Jun 2026 23:00:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e4ff25d146edff2a177dad83f2b8ad9e69aae3796057c444466305f9ed7110`  
		Last Modified: Tue, 16 Jun 2026 23:00:24 GMT  
		Size: 108.3 MB (108294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a881ed15568178537604cf1215ad131ae1bccf67d610c93cc871868760514cac`  
		Last Modified: Tue, 16 Jun 2026 23:00:22 GMT  
		Size: 21.0 KB (21006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c947ae7d6245f16f8532db4ebb8aa3026098678195236620c7df899e9b002d`  
		Last Modified: Tue, 16 Jun 2026 23:00:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69528baa9aeb307409501e9085056697c4073191e1d6225169b4c2d827233569`  
		Last Modified: Tue, 16 Jun 2026 23:00:23 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f521e643fff9cfb30b01e604b4c9e050bd685460d55a5ade5635dc7c8d0b93`  
		Last Modified: Tue, 16 Jun 2026 23:00:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:ff67ded597c240336ebf610bc0ff42fd415368701bf3beae4ab64b7cc8a820d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.8 KB (654786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f254d19090058a9d1052b45e13c5313bcd66cd652013b6646319c44e69c1f01b`

```dockerfile
```

-	Layers:
	-	`sha256:9e5903792700ebccfec2a13cb0bd7bf30b3304ad7483a49ed35b1b15b18d5921`  
		Last Modified: Tue, 16 Jun 2026 23:00:22 GMT  
		Size: 615.1 KB (615130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:530de2e909e5fee97c885b05fd89c35dd833a9fb69f7e61a05ec12ff849a077b`  
		Last Modified: Tue, 16 Jun 2026 23:00:21 GMT  
		Size: 39.7 KB (39656 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:060b983d17345a52fb5baae539d674bdaccba5b07ef99ca07aa13bd990200504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121327132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbb05dd02a8ace9ac0fc0079aab227d74dc089275b5fe14d3183b1ff3f4a5eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:31 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:57:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:57:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:57:34 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:57:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:57:34 GMT
ENV PG_MAJOR=19
# Tue, 16 Jun 2026 22:57:34 GMT
ENV PG_VERSION=19beta1
# Tue, 16 Jun 2026 22:57:34 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Tue, 16 Jun 2026 22:57:34 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 22:59:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 22:59:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 22:59:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 22:59:59 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Tue, 16 Jun 2026 22:59:59 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 22:59:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 22:59:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 22:59:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 22:59:59 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 22:59:59 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 22:59:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67aa5445635c2070ddcd942b909ec188e484afa9d66138123fd1ea74a5f4e29`  
		Last Modified: Tue, 16 Jun 2026 23:00:15 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebbb3a4e14488731cb8eeb9c4149ed34a14c6c5619e6129f34edfe44dabeb5c`  
		Last Modified: Tue, 16 Jun 2026 23:00:15 GMT  
		Size: 874.7 KB (874708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0678ad862f262392121e9fde56038bcaaa2842d8c3aedb45cc44e200a615e03c`  
		Last Modified: Tue, 16 Jun 2026 23:00:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28da852a8f09dfbdb8d4af529e5a16fc7532bb615778aab467cac49e8f7be408`  
		Last Modified: Tue, 16 Jun 2026 23:00:18 GMT  
		Size: 116.2 MB (116224050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da7da1bc40608dada2f90b03408fd0af1a1d48360b0b266fc7fec0c37435ab8`  
		Last Modified: Tue, 16 Jun 2026 23:00:17 GMT  
		Size: 21.0 KB (21006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76d852804da551d339adfc01aef240e4806b6832871bb384081e71dff7f5608`  
		Last Modified: Tue, 16 Jun 2026 23:00:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ab935754387961623a8790f8e6cfe0e03f14bbf13325c98cc89f672e27d994`  
		Last Modified: Tue, 16 Jun 2026 23:00:17 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f585d7481d56052363cafedb18860cb43033b6570909fc8406784103aeac00`  
		Last Modified: Tue, 16 Jun 2026 23:00:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:2f32075e2f30121da5d57406717748d4d197def95a9349b9cbb215853719667f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.8 KB (654818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1027b750b4d55f4db3372500b8e07d5c1c26aa435d7e98538291cb8a9a55ebbd`

```dockerfile
```

-	Layers:
	-	`sha256:53f203f6a204d14f9c67acf57558cfc6eb28b4a8250b3580f55a6d80176d66a2`  
		Last Modified: Tue, 16 Jun 2026 23:00:15 GMT  
		Size: 615.1 KB (615138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3adebeac74b002ba00ec94145441503146f5eba114ca3e0046ee1ca7d12e8fc`  
		Last Modified: Tue, 16 Jun 2026 23:00:15 GMT  
		Size: 39.7 KB (39680 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.23` - linux; 386

```console
$ docker pull postgres@sha256:26153f0ff57d3a28b7223abe6daae9652aa9b04d605ea6737cf89037c13fe7c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130011588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5e8bbe9fa0c0453ff01a1d7f5bfe3cb77bcab17b98ced1a983e14d9f19b59c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:49 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:57:52 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:57:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:57:52 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:57:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:57:53 GMT
ENV PG_MAJOR=19
# Tue, 16 Jun 2026 22:57:53 GMT
ENV PG_VERSION=19beta1
# Tue, 16 Jun 2026 22:57:53 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Tue, 16 Jun 2026 22:57:53 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:39 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Tue, 16 Jun 2026 23:00:39 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:39 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:39 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ff68f24241ae16dec2fc520ee0cbb032e2874b644bbd866dea356eb335a996`  
		Last Modified: Tue, 16 Jun 2026 23:00:56 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba35026546ce25b6d27fec38934f470210e36227af835bf20a019f181686c59`  
		Last Modified: Tue, 16 Jun 2026 23:00:57 GMT  
		Size: 891.6 KB (891650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9ee48591084fa70748fd476da612f648db9e2107623d78212aa57aa2094957`  
		Last Modified: Tue, 16 Jun 2026 23:00:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527f4fa08360eb6fa94e6b8822fd09976fda90d95518a345c07886bd414dc019`  
		Last Modified: Tue, 16 Jun 2026 23:00:59 GMT  
		Size: 125.4 MB (125400992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7915464aeede78e48544beb870a54734aaa19e1fb49f8716d0d9c8b424bf47`  
		Last Modified: Tue, 16 Jun 2026 23:00:58 GMT  
		Size: 21.0 KB (21005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e195648c6d46d027f8e14e349ac2e8e41d08ac053a042ffcd38413ef243d74c8`  
		Last Modified: Tue, 16 Jun 2026 23:00:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ca1a4daa54bffb8f8a70201160da6cf3f7be981193e7adfc548fd29bedf63c`  
		Last Modified: Tue, 16 Jun 2026 23:01:00 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11b5d691d8cbcd18b65a076cb076d73545e1d7863b4a74ce2ed2078e8c65e4b`  
		Last Modified: Tue, 16 Jun 2026 23:00:59 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:414467fd592096df82cb5b966e23bfdef95069544ae6744664f0bc06bb10587a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.3 KB (655251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83fc5a925a127c0bc9d5c3f6b116cb5f8209aded2e955594b9278e9f5338b5a7`

```dockerfile
```

-	Layers:
	-	`sha256:34a3025d332588a9138a82d15313f18d18ae651a6a9333904b2fe55d816ac86a`  
		Last Modified: Tue, 16 Jun 2026 23:00:56 GMT  
		Size: 615.8 KB (615758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98d86b846688c04f27e8a481fccbfc74c20b32ceb8da9993a11a8407d0d3a63a`  
		Last Modified: Tue, 16 Jun 2026 23:00:57 GMT  
		Size: 39.5 KB (39493 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.23` - linux; ppc64le

```console
$ docker pull postgres@sha256:6a334310a9919eca8aef32cc3208b16b8e119dbbca52e267fa9aa7835f9045ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126185054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b35ac0f9c2664cffb0381c24de5d93db99bf4b8c47f5d852e7a49aa76746133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:56:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:56:30 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:56:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:56:30 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:56:31 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:56:31 GMT
ENV PG_MAJOR=19
# Tue, 16 Jun 2026 22:56:31 GMT
ENV PG_VERSION=19beta1
# Tue, 16 Jun 2026 22:56:31 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Tue, 16 Jun 2026 22:56:31 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:54 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:56 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Tue, 16 Jun 2026 23:00:56 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:56 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:56 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeb214de6218b60491f673adf9db82be71ea034b0f77f7368c52371e738b5b2`  
		Last Modified: Tue, 16 Jun 2026 23:01:33 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6afa0b71083646c91abee705158ea148e7247c5befb4dabd9b4d97a65cfb4b`  
		Last Modified: Tue, 16 Jun 2026 23:01:33 GMT  
		Size: 880.1 KB (880129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301da0e7fa1c03833d438a0704514f0a9b1269117d1e36308f156f140fbd8f27`  
		Last Modified: Tue, 16 Jun 2026 23:01:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1f6568f169a863ab7cd57c5a2d57771d8f6c95d00aece655ed3f2395b4718c`  
		Last Modified: Tue, 16 Jun 2026 23:01:37 GMT  
		Size: 121.4 MB (121445492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ff0524adc331c22637868dc6e1a40df8071165b671bffa152219de9c8375b6`  
		Last Modified: Tue, 16 Jun 2026 23:01:34 GMT  
		Size: 21.0 KB (21008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c6d5a5312ca372ca6fefb0b807ad719182a5e3ad8210202ead4b4ddb7646e0`  
		Last Modified: Tue, 16 Jun 2026 23:01:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3049eac49763c68a8933963d7356bbc637187a017ecc4a8ea2d92b09af6184`  
		Last Modified: Tue, 16 Jun 2026 23:01:35 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16e4c950b5482a291356cdc85111426dd9797f49abc133156ee10aaa389bb48`  
		Last Modified: Tue, 16 Jun 2026 23:01:36 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:a4507dbf37ab630cfe433f1629bbf69884fff78fddafcc8d11962181e01c6db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.0 KB (653031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1eb6d338465dba0b53a3c694a5542d941077d9b7a3b37f9eca5940fb90e3a0`

```dockerfile
```

-	Layers:
	-	`sha256:2792b6240b8be68dd36885735932c92f379b9764659c67dddbf5770ccac19138`  
		Last Modified: Tue, 16 Jun 2026 23:01:33 GMT  
		Size: 613.5 KB (613471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f90cf72a704df4be45c3e23077eebd6f4672a5d9ae28bb5829e0d35606107757`  
		Last Modified: Tue, 16 Jun 2026 23:01:33 GMT  
		Size: 39.6 KB (39560 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.23` - linux; riscv64

```console
$ docker pull postgres@sha256:2f5630d1578b9ef3fccc681081a72db68fec60812532f3e8e4f975027b421186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116763446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4185b2f47556fa9eff7c5a2e5e1b04ed38426cd4fabcfe3142df70accbb9091`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Sat, 06 Jun 2026 10:50:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 10:50:28 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 10:50:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 10:50:28 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 10:50:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 10:50:28 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 10:50:28 GMT
ENV PG_VERSION=19beta1
# Sat, 06 Jun 2026 10:50:28 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Sat, 06 Jun 2026 10:50:28 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 06 Jun 2026 11:42:04 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 06 Jun 2026 11:42:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 11:42:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 11:42:05 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 11:42:05 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 11:42:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 11:42:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 11:42:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 11:42:06 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 11:42:06 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 11:42:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7df039f81d0d1157153d6a10d87825ed680c09316ad14754246d92e580683b`  
		Last Modified: Sat, 06 Jun 2026 11:45:03 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2a8c7ef4a7e5db1d384052a59b67dbc6a94ac5b2ba0cdd6cf72d3b6c767784`  
		Last Modified: Sat, 06 Jun 2026 11:45:04 GMT  
		Size: 867.5 KB (867539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8afd435738b3e5c8a24e3e7b16535a142b2da6735e29ec0bd3bd54087e793ea`  
		Last Modified: Sat, 06 Jun 2026 11:45:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10343b79618d279bae769ca805ae925f620f6e48adb52250482aef54a215b1e`  
		Last Modified: Sat, 06 Jun 2026 11:45:21 GMT  
		Size: 112.3 MB (112279729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950e77c4da2ca727e71073dd12ac112cdd16ea58672a8eddc1b0f355d35a2e2c`  
		Last Modified: Sat, 06 Jun 2026 11:45:05 GMT  
		Size: 21.0 KB (21012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad25e0626d1b7cebcd5448c70884b138475f66cc245a787b072676c5fc919720`  
		Last Modified: Sat, 06 Jun 2026 11:45:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df879552b7a39e2b40cf60f7df412ed4796e51ecbc65971256255e905786c60f`  
		Last Modified: Sat, 06 Jun 2026 11:45:05 GMT  
		Size: 6.1 KB (6104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc5adddf8259a918fddfca055ab072528f35fcfff8e2ac022573e1353c47109`  
		Last Modified: Sat, 06 Jun 2026 11:45:07 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:098bd30ab8acf8688b492fc0a0a0d0faedad62d02ec12d64673068ceace90536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.4 KB (655365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c6a7abb84d9ba5b6f10fcb7926b494038e67d00f8e520c07d457976258d713`

```dockerfile
```

-	Layers:
	-	`sha256:fe772b54c913629b98551d286d4386cff182fb74bb916c7471aec76c9521d828`  
		Last Modified: Sat, 06 Jun 2026 11:45:03 GMT  
		Size: 615.5 KB (615481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf6d761d515f52343e2cdbd5bffadfff9ba35479190564c25460f6788031e61`  
		Last Modified: Sat, 06 Jun 2026 11:45:03 GMT  
		Size: 39.9 KB (39884 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.23` - linux; s390x

```console
$ docker pull postgres@sha256:f95afcc6372dfb59da8c0815b27fec2b8e8a72e981b72da95f73b31640bd05e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129624226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b141827eebfa3d47d1e4620f428932a6ca744ebde4fc79f3532d92319b658268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:56:31 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:56:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:56:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:56:34 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:56:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:56:35 GMT
ENV PG_MAJOR=19
# Tue, 16 Jun 2026 22:56:35 GMT
ENV PG_VERSION=19beta1
# Tue, 16 Jun 2026 22:56:35 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Tue, 16 Jun 2026 22:56:35 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:01:19 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:01:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:01:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:01:20 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Tue, 16 Jun 2026 23:01:20 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:01:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:01:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:01:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:01:20 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:01:20 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:01:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138f17cbec7383c2f4e65ac61d6338f7eaa0091aa05691e282fa28a8f1f0806a`  
		Last Modified: Tue, 16 Jun 2026 23:01:46 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc13189f654454854b34853fccf423aefa764a77d0f758bd423b7bc8cb09ac`  
		Last Modified: Tue, 16 Jun 2026 23:01:46 GMT  
		Size: 895.8 KB (895799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffce3484740bdf0a190bad848828fb524b0b4902f37de1c2c0b810cf6e2c36ce`  
		Last Modified: Tue, 16 Jun 2026 23:01:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b20c5085f7303d9b5002991629dcf9effdc0d5af442461a94db1d1172d8e93f`  
		Last Modified: Tue, 16 Jun 2026 23:01:48 GMT  
		Size: 125.0 MB (124973387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94509169c924bf2d85719e810fe028c03b5adfaab24d584d0dee4121be3048f3`  
		Last Modified: Tue, 16 Jun 2026 23:01:47 GMT  
		Size: 21.0 KB (21005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e216abee6dfe5593331cdeeb06039ebfa13a195d8b534d8d1f7da2149c004d5`  
		Last Modified: Tue, 16 Jun 2026 23:01:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78915a594821d006c500baca1b8635533baeddb9c46a863416acf37d1348569d`  
		Last Modified: Tue, 16 Jun 2026 23:01:47 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c257b966ac3ec4975b70ceb8deff0d7d266a12f4b88088228b3c27007997fd2e`  
		Last Modified: Tue, 16 Jun 2026 23:01:48 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.23` - unknown; unknown

```console
$ docker pull postgres@sha256:8e68a936d6ea5ada7fdf5b9b1bdfdd514a551f685cb06669ba57b8b6a4521b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.6 KB (654639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b0633f32e5e2221e71d88985436c46d03ce1e781c1280d3e953f1e682e8a1d`

```dockerfile
```

-	Layers:
	-	`sha256:7db4bc5e9948bfa0d18068c4caecb81ab722bb0cf8d72dd4ecb7b26ed2a00e30`  
		Last Modified: Tue, 16 Jun 2026 23:01:46 GMT  
		Size: 615.1 KB (615117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b801d31a5b4f77c7399f277975c874cd35d85785eb8c8d3142de52faeea3c07c`  
		Last Modified: Tue, 16 Jun 2026 23:01:46 GMT  
		Size: 39.5 KB (39522 bytes)  
		MIME: application/vnd.in-toto+json
