## `postgres:alpine3.22`

```console
$ docker pull postgres@sha256:06f99695cdbfba50a9d19073e2c2af16b8995ee846d25119d992ad719818522b
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

### `postgres:alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:5d4fe8f50aaf236e5e4463cd377ea7e0bf22e2ed384512b8da7e08fb105d16d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111518807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1873db7f1638e5d04cc510ca2dcc79e1ce095db581ed1bbd3034fe1524d2c141`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:03:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:03:58 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:03:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:03:58 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:03:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:03:59 GMT
ENV PG_MAJOR=18
# Thu, 12 Feb 2026 21:03:59 GMT
ENV PG_VERSION=18.2
# Thu, 12 Feb 2026 21:03:59 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Thu, 12 Feb 2026 21:03:59 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:06:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:06:28 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:06:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:06:28 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 12 Feb 2026 21:06:28 GMT
VOLUME [/var/lib/postgresql]
# Thu, 12 Feb 2026 21:06:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:06:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:06:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:06:28 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:06:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:06:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f9d48f020863b7ed2ce64d7a70c1af2c7e78c4ed1a89d7fbbddc876b08c2a3`  
		Last Modified: Thu, 12 Feb 2026 21:06:45 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63fc7e93f09237bce2daa06ff9c1af6b7a01fc362c276d6b3a5d30f9639586b`  
		Last Modified: Thu, 12 Feb 2026 21:06:45 GMT  
		Size: 918.3 KB (918291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a545683a0dc0bf1e4a11bf62b06e44325de072b27eaafed8893b32ff805fa6e`  
		Last Modified: Thu, 12 Feb 2026 21:06:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223fe13e3dc4e3410e1aa0845975e2b32bdb5c1b971d6570e1587e717ad98b44`  
		Last Modified: Thu, 12 Feb 2026 21:06:47 GMT  
		Size: 106.8 MB (106769479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a56d9d2742f5238aaef1bd4dcb80e09275014aa0ecaeabdffb527433a290b9f`  
		Last Modified: Thu, 12 Feb 2026 21:06:46 GMT  
		Size: 18.9 KB (18921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49f0415eeaa55a5458b3401ca99b0615524c3682809dae053e990c9fc73bcbf`  
		Last Modified: Thu, 12 Feb 2026 21:06:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28474c2e6a4d9d73f1699ba31f7b8cbe7dad58b858863c44fe13c8c920b3ef51`  
		Last Modified: Thu, 12 Feb 2026 21:06:46 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b949e93772acbd518e32b55b44452913c1dca5a30ca55f487941cb3672895163`  
		Last Modified: Thu, 12 Feb 2026 21:06:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:0eb06c5c7965d6ed94ec2e16dc54cde72f39ac3f7bcc808b0cc94d90d4b3d68d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.9 KB (637870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565cf4a3d5725330bfc812c4e0c67851e97c6325f1909b1d8772291338e923cb`

```dockerfile
```

-	Layers:
	-	`sha256:670f3bdac8022598401a085387cfbe08a16736c728907381b10567db6eb2ea0c`  
		Last Modified: Thu, 12 Feb 2026 21:06:45 GMT  
		Size: 598.2 KB (598244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:372be2acac3a3855d56eadfbfb6635c230725d9d0b96e402da9da31a266730fc`  
		Last Modified: Thu, 12 Feb 2026 21:06:45 GMT  
		Size: 39.6 KB (39626 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:2489189ede2b042a1d7891f9cdc1441cb7257b1f4cf3f0b17b1218136b99c6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91100772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090792d6976ea25932d0f15249d32a998358405416435e9ecfc59203e1e67c56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:20:18 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:20:24 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:20:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:20:24 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:20:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:20:24 GMT
ENV PG_MAJOR=18
# Thu, 12 Feb 2026 21:20:24 GMT
ENV PG_VERSION=18.2
# Thu, 12 Feb 2026 21:20:24 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Thu, 12 Feb 2026 21:20:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:23:21 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:23:21 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:23:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:23:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 12 Feb 2026 21:23:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 12 Feb 2026 21:23:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:23:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:23:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:23:22 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:23:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:23:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151a63d51d4af742d8e67ef5925f02ae6fa3adb1d8cbc015020af6e4f50ad54`  
		Last Modified: Thu, 12 Feb 2026 21:23:32 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407e35b496f9c1c7676831c92727d61ecaefb7c60efae9e6d3178489595db4e4`  
		Last Modified: Thu, 12 Feb 2026 21:23:32 GMT  
		Size: 886.1 KB (886132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f3e6c705c81c168edfd32ccdcc2965c2d429d0274f93ba54cffcf2fb2ae1cb`  
		Last Modified: Thu, 12 Feb 2026 21:23:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77696751b7d6a178228fa22c9e67ed6de57dd9514e6199cac0f0cc75e2312b84`  
		Last Modified: Thu, 12 Feb 2026 21:23:34 GMT  
		Size: 86.7 MB (86683441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cb0890820058063e95303c35f4482e18c976942a16be2525a841619f97f3bc`  
		Last Modified: Thu, 12 Feb 2026 21:23:33 GMT  
		Size: 18.9 KB (18917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58965b69a96c9e497d42184f1ffce5e72f257408ece0eea0a9bbdf368387a8a`  
		Last Modified: Thu, 12 Feb 2026 21:23:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffdc3792604a46b3b9a04c55d4c61ef7059d203c4ade1bb244d0a541cf3343e`  
		Last Modified: Thu, 12 Feb 2026 21:23:33 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a34472eea1449423ec99a74880b352737518e5e58e83946cfdbefda91b66f0`  
		Last Modified: Thu, 12 Feb 2026 21:23:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:40a3420c2fde03abfb5b7f8f1e36feaec58b4a1b22f96faf2ac2b3c836d8685c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea59ae0da6c50353008f684e4f6c77189e199f023331f589b9fd6366fe25f3de`

```dockerfile
```

-	Layers:
	-	`sha256:ae1bcf2a9f8392f9ce78cdcf594ada096bbcbd6ac14ae79b491a7fa542477481`  
		Last Modified: Thu, 12 Feb 2026 21:23:32 GMT  
		Size: 39.6 KB (39556 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:ff7c0bda16051f7aa4ff12bb192656f9881fef7a25635bc41bb13d954d650201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86292797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70e75b893207aef69d61e3fa1e6385452ff6aa804fd185210132b2de2173e86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:16:49 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:16:55 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:16:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:16:55 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:16:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:16:55 GMT
ENV PG_MAJOR=18
# Thu, 12 Feb 2026 21:16:55 GMT
ENV PG_VERSION=18.2
# Thu, 12 Feb 2026 21:16:55 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Thu, 12 Feb 2026 21:16:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:19:51 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:19:51 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:19:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:19:51 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 12 Feb 2026 21:19:51 GMT
VOLUME [/var/lib/postgresql]
# Thu, 12 Feb 2026 21:19:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:19:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:19:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:19:51 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:19:51 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:19:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf298e7bac23076f867c0df7486912dfb7c6e51db29674c45938bd839553afc`  
		Last Modified: Thu, 12 Feb 2026 21:20:03 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48aad8f2d0f425ac5dfb0a182233fd039ac3c619f7db14f7a20c7cc3bbc9b611`  
		Last Modified: Thu, 12 Feb 2026 21:20:03 GMT  
		Size: 886.1 KB (886136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee080a49145bba92231a47178347943ff7ac389837607de7e0a91df903ba546b`  
		Last Modified: Thu, 12 Feb 2026 21:20:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c994c1af169e658f87413d3984773debb39e2b7be6a4ab11af77a26f89fd7a7c`  
		Last Modified: Thu, 12 Feb 2026 21:20:05 GMT  
		Size: 82.2 MB (82156872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24109eac7ffe4d6db7280d9a1a1d023541195571aaf8948680b3ffd168d838d`  
		Last Modified: Thu, 12 Feb 2026 21:20:04 GMT  
		Size: 18.9 KB (18920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462b0e1b02790047415a75877873d3067058d85167eb6d2fc9a1fab277837473`  
		Last Modified: Thu, 12 Feb 2026 21:20:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31197be1f8cf7987192d3a72556acb7b9bb1c09efff8e0a0f893f213361a5da`  
		Last Modified: Thu, 12 Feb 2026 21:20:04 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac91a6630ac1b6b6144a06ed64cf85b049832139c9ed725adc22e0185d3883c`  
		Last Modified: Thu, 12 Feb 2026 21:20:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:d4c660f32025298ecd6d674c9cfdd8f00054496d3db9d71343350f4d1586f6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.0 KB (638042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a614fd3fb457e2bbd7a6110d2563052b5205b0c72455958d5b5e9cac0d089776`

```dockerfile
```

-	Layers:
	-	`sha256:849a49cb8cac1618d2e30d4bb4b1fc75869d26f6f90121902e1034c242c3a86e`  
		Last Modified: Thu, 12 Feb 2026 21:20:03 GMT  
		Size: 598.3 KB (598272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c84b20f9da6576d5cbe45e52d48664b6166080ed9b0bb933362becb9bdf2515`  
		Last Modified: Thu, 12 Feb 2026 21:20:03 GMT  
		Size: 39.8 KB (39770 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:054d2bcc6666bffac6dedd28b8cf07eafeadaae23e52ce62cf1dd98ef8a13b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107487330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdeeb5e8157e6f2c5f53de7bfb4e4274d7cb78a74efdbee41073d300134a4ca3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:04:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:04:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:04:08 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:04:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:04:08 GMT
ENV PG_MAJOR=18
# Thu, 12 Feb 2026 21:04:08 GMT
ENV PG_VERSION=18.2
# Thu, 12 Feb 2026 21:04:08 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Thu, 12 Feb 2026 21:04:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:06:35 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:06:35 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:06:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:06:35 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 12 Feb 2026 21:06:35 GMT
VOLUME [/var/lib/postgresql]
# Thu, 12 Feb 2026 21:06:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:06:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:06:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:06:35 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:06:35 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:06:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b3c6b59c5febcaf3f5da1f3059143be3e22d21f7adf103e5e7b1c5b9c6e065`  
		Last Modified: Thu, 12 Feb 2026 21:06:50 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7252666ea5cdf07b59cbe1ea5e0fb3001d7e0e1ef811b95b7f22972c5fc9049`  
		Last Modified: Thu, 12 Feb 2026 21:06:50 GMT  
		Size: 873.5 KB (873484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ac4b8f0716c1f36978933254c596f7dbe7590f89794ef804a5c47f2b4b6c61`  
		Last Modified: Thu, 12 Feb 2026 21:06:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e372c4946f0b62cb2f7f45498378ef8e01dd843264c62bd186ce1d0feac62ad5`  
		Last Modified: Thu, 12 Feb 2026 21:06:52 GMT  
		Size: 102.4 MB (102448163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06f8f6da2e84f8c961325af7fa00e0e36977bbc26e84d18cbceaba043b3523d`  
		Last Modified: Thu, 12 Feb 2026 21:06:51 GMT  
		Size: 18.9 KB (18926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d775545f1143d3c6940f543b4e0b75b825043c3a31f6262163946e1b361596`  
		Last Modified: Thu, 12 Feb 2026 21:06:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151ddaf23a16b636a6417f6eecc8dac04bcc6740ab68a6a317ba6d94f13fdee7`  
		Last Modified: Thu, 12 Feb 2026 21:06:51 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5eecffe6477059ca5047eac1ec22236e0f065648e1e3a8186b7c2bc9982363a`  
		Last Modified: Thu, 12 Feb 2026 21:06:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:e915abc1890d886117b350ee591986e0328a3d3822613350f4d52330eddb8c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.1 KB (638095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900de4b2163f5c8cf3d40756604a07d3928822acf18d3b35b7b88b97a31cae33`

```dockerfile
```

-	Layers:
	-	`sha256:eb6a189628ca3641fa3cadaf3dfea236c8a04ecf38d95a1c755057e4b68b8997`  
		Last Modified: Thu, 12 Feb 2026 21:06:50 GMT  
		Size: 598.3 KB (598288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2324ac8ea355f1acaf908a5c48ff97be760180ae4156eea3c5805d2d5a54e499`  
		Last Modified: Thu, 12 Feb 2026 21:06:50 GMT  
		Size: 39.8 KB (39807 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:7f2cf57fbfb5b3a9d3548c71e3fd790fe85199dcc8d5c74039904b27f65fc118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117894449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9e7e02c1825478226a40a564960033a3d256aeb813f3313bafb15090b09758`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:04:21 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:04:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:04:26 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:04:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:04:26 GMT
ENV PG_MAJOR=18
# Thu, 12 Feb 2026 21:04:26 GMT
ENV PG_VERSION=18.2
# Thu, 12 Feb 2026 21:04:26 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Thu, 12 Feb 2026 21:04:26 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:07:10 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:07:10 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:07:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:07:10 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 12 Feb 2026 21:07:10 GMT
VOLUME [/var/lib/postgresql]
# Thu, 12 Feb 2026 21:07:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:07:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:07:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:07:11 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:07:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:07:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4774a19bdfa8b8c0f2f63610df2dfacc902ca2377cc4a661e4e6f1d5b068d36d`  
		Last Modified: Thu, 12 Feb 2026 21:07:25 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f369115422943494bc169ca36aca191e05c9dd878337fc030bb2500a90f49b`  
		Last Modified: Thu, 12 Feb 2026 21:07:25 GMT  
		Size: 890.6 KB (890634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daa55d920625364415c0b1c8fb59d925ea865b6288b336fc75f2dbf655af1fc`  
		Last Modified: Thu, 12 Feb 2026 21:07:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fd35778a915a2a3ed2fcdb09d8bd0d12f56738fe010fb9b15ff4b0c59667b4`  
		Last Modified: Thu, 12 Feb 2026 21:07:28 GMT  
		Size: 113.4 MB (113356927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3480a20e4a9c9b8d873503abe356d1e5a52399ad3944d82809972925b74985`  
		Last Modified: Thu, 12 Feb 2026 21:07:26 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e105e02261a33c8b6e3984a686a4b24e26759a4f98c62b6171805435039bdb2`  
		Last Modified: Thu, 12 Feb 2026 21:07:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f743587f93da40a7e8d983d3259f989c7112b5e368858ead69adc1f10046875b`  
		Last Modified: Thu, 12 Feb 2026 21:07:27 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2695f4b1fb3b07a7f922c9928f10804f7665eec933d4cba998f9c82c35f7f0`  
		Last Modified: Thu, 12 Feb 2026 21:07:28 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:ad5db8698c96f61f9b385fe0a20a447bfb876292fe5be0352e99ad50e5140329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 KB (637810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebc77bb0537196cca4e16ad1267d4d1f5411383526014ebfb35c91eb715f4e2`

```dockerfile
```

-	Layers:
	-	`sha256:875b53e9e428363a02c8ea0470e4531291b87104def792644041dd19c02e8075`  
		Last Modified: Thu, 12 Feb 2026 21:07:25 GMT  
		Size: 598.2 KB (598224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8476e5293b26ff92497e3ac0dbc8ddb2fa8dda6dcb3c624e7a5f31ca7f02a6fa`  
		Last Modified: Thu, 12 Feb 2026 21:07:25 GMT  
		Size: 39.6 KB (39586 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:9f9b28c03f1bb78c1c3db82ce691f9acd4b9b8da7fb5535f7376313418bcbc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95450357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddda44433e3025ddb565458f12fc6bc5d75b4675c24c721759a26e84c024835`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:06:00 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:06:12 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:06:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:06:12 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:06:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:06:12 GMT
ENV PG_MAJOR=18
# Thu, 12 Feb 2026 21:06:12 GMT
ENV PG_VERSION=18.2
# Thu, 12 Feb 2026 21:06:12 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Thu, 12 Feb 2026 21:06:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:10:36 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:10:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:10:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:10:38 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 12 Feb 2026 21:10:38 GMT
VOLUME [/var/lib/postgresql]
# Thu, 12 Feb 2026 21:10:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:10:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:10:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:10:40 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:10:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:10:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c65175e4a78e75c1adc1c569354fe719e50457fdbdd1612adccbd559da08c1`  
		Last Modified: Thu, 12 Feb 2026 21:11:11 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47af42dfcd093de1f52666dfa1cb8ed4291e124998435eea188cac1feb2ef729`  
		Last Modified: Thu, 12 Feb 2026 21:11:11 GMT  
		Size: 879.0 KB (879036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8773caba0cc71f1241c5d1fb6e8c3b7afa6a89200a7975c71ffbf3112756a3`  
		Last Modified: Thu, 12 Feb 2026 21:11:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6ffffd3fac4a8bff04a0f28209f0f6e49531a3addd3ea1cb0d43bf9a3bf5b0`  
		Last Modified: Thu, 12 Feb 2026 21:11:14 GMT  
		Size: 90.8 MB (90810851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b838b6edbb8190d3c59e234d4037d1d3d2f86fcdd36d79e74ca639bda326280c`  
		Last Modified: Thu, 12 Feb 2026 21:11:12 GMT  
		Size: 18.9 KB (18928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ad3ff45871674670487f15e3eeb8a6a9cc977c939101fe9b107d0166a68bff`  
		Last Modified: Thu, 12 Feb 2026 21:11:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1e9cbe303eaa9bf8a4b7299c962d1a65ce5f88b792be5e7f4a1c981dd9d727`  
		Last Modified: Thu, 12 Feb 2026 21:11:13 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a4ea7d630e031fe7e04cae01e296a91624e53a1f326534fba5e9552e020c8c`  
		Last Modified: Thu, 12 Feb 2026 21:11:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:cd7e78453ea6d92173d2ad2f84074eb7d084a7dccfac71cd38be8eca89d7bae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.3 KB (634330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0893b5433ec3b851973e326e55e0d7b5e4b9c01ee6e7d4ea1d85a9e23dcdabdb`

```dockerfile
```

-	Layers:
	-	`sha256:0ec6b1f2ad5fae62edee5db1072b7aa8dbe0cce7ee80e5bdd2fd8b5c18182c3a`  
		Last Modified: Thu, 12 Feb 2026 21:11:11 GMT  
		Size: 594.7 KB (594659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c925632827c6af0ee3423f3eaaf0e960c8ead09a604b5b577ad4ae15caff806`  
		Last Modified: Thu, 12 Feb 2026 21:11:11 GMT  
		Size: 39.7 KB (39671 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:d225bb87ba269f9be666089d67e0516aca40f176c6be802f4c0b42153962b627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111727785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45601fbcba8c17818eb4cc206c643a88de41948c61f76a90ccd47747de6f615`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Fri, 13 Feb 2026 00:03:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 13 Feb 2026 00:03:22 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Feb 2026 00:03:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Feb 2026 00:03:22 GMT
ENV LANG=en_US.utf8
# Fri, 13 Feb 2026 00:03:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 13 Feb 2026 00:03:22 GMT
ENV PG_MAJOR=18
# Fri, 13 Feb 2026 00:03:22 GMT
ENV PG_VERSION=18.2
# Fri, 13 Feb 2026 00:03:22 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Fri, 13 Feb 2026 00:03:22 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 13 Feb 2026 00:52:36 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 13 Feb 2026 00:52:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 13 Feb 2026 00:52:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 13 Feb 2026 00:52:37 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 13 Feb 2026 00:52:37 GMT
VOLUME [/var/lib/postgresql]
# Fri, 13 Feb 2026 00:52:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 00:52:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 13 Feb 2026 00:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Feb 2026 00:52:38 GMT
STOPSIGNAL SIGINT
# Fri, 13 Feb 2026 00:52:38 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 13 Feb 2026 00:52:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9a8d29c18a7aa35e1e673e585403324e4011c659e3a9af9631eeef53eb1abe`  
		Last Modified: Fri, 13 Feb 2026 00:55:28 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f6ced6daa9dca5801962fab9724b150e63d0b23f3667a8a57104fdc08d51d`  
		Last Modified: Fri, 13 Feb 2026 00:55:28 GMT  
		Size: 866.6 KB (866630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778a0da493e5086a70feef9ef732427bd2c927a4c5e0b6cb88e9e6e2f5d4d72a`  
		Last Modified: Fri, 13 Feb 2026 00:55:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3f0c56c7c7f551b6c19b7eca966f4ff5396da163f8b3b61251260cb3ddc31b`  
		Last Modified: Fri, 13 Feb 2026 00:55:44 GMT  
		Size: 107.3 MB (107317562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243c1d8d5af39b88a9ab392ebd6f01002778cf9f05374d48c72e49969f3870d7`  
		Last Modified: Fri, 13 Feb 2026 00:55:29 GMT  
		Size: 18.9 KB (18927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5ca958eaf5bb7d42a36066615639b2143c67ab25eb46cde27a6861cfea167`  
		Last Modified: Fri, 13 Feb 2026 00:55:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554d12ede0c0532982d38f86e621ad5c47a35f34257261219fac196dee629d19`  
		Last Modified: Fri, 13 Feb 2026 00:55:30 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb2c78269a8e1c7284b118a6cc4cb5481f1f64c9f834901babac720f79b6eb`  
		Last Modified: Fri, 13 Feb 2026 00:55:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:f4499c7d71f55b8f88cc0862e150eec501987a031b5715609bce5681d7528fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 KB (635992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23524e7b8bb40b0dd9dcd585e8f8b826ba0d722d32ad766f9dd416b2d8cf071`

```dockerfile
```

-	Layers:
	-	`sha256:5f278d6512a6d0f72ec39caf99442de8b97985016effe89e3592477413bb6f1b`  
		Last Modified: Fri, 13 Feb 2026 00:55:28 GMT  
		Size: 596.3 KB (596317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af88d5a165f9036e5ac5024f48d0d9c8b32b2a6a1da2566243a5b2469fd3f39`  
		Last Modified: Fri, 13 Feb 2026 00:55:28 GMT  
		Size: 39.7 KB (39675 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:c47d87139dd9ece6d15d2a500b61c09dac98798aa1a8094c325b1962730b0ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120297913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b908545c39e47f61ca6e96a8de8a8ec64c57360dbe0aa1eb708896f3c4fd8335`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:02:33 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:02:37 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:02:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:02:37 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:02:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:02:38 GMT
ENV PG_MAJOR=18
# Thu, 12 Feb 2026 21:02:38 GMT
ENV PG_VERSION=18.2
# Thu, 12 Feb 2026 21:02:38 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Thu, 12 Feb 2026 21:02:38 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 12 Feb 2026 21:05:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:05:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:05:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:05:52 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 12 Feb 2026 21:05:52 GMT
VOLUME [/var/lib/postgresql]
# Thu, 12 Feb 2026 21:05:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:05:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:05:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:05:52 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:05:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:05:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de5ab441dabb81e9ca143b33f430fcde023e7641b4434052405ebb7c2c0434e`  
		Last Modified: Thu, 12 Feb 2026 21:06:17 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a1da40c4ec0399caebc58e7630eee7f84ed9d37fc332bef6e8ad2882c4e04b`  
		Last Modified: Thu, 12 Feb 2026 21:06:17 GMT  
		Size: 894.4 KB (894409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17aa5adf39a06c5e976f41a2e570538eeee2fa378dc20c16fd22fd3debc2a26d`  
		Last Modified: Thu, 12 Feb 2026 21:06:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7140fc495a65de9da0ddcb5112606c1e12e100224ac5651a0779f3e1eec4d91e`  
		Last Modified: Thu, 12 Feb 2026 21:06:22 GMT  
		Size: 115.7 MB (115726919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91dff42e1cc2319f5ff8e718f6ff3e08d1e0e0b8cf9b3f8eff5e01623e179ffc`  
		Last Modified: Thu, 12 Feb 2026 21:06:18 GMT  
		Size: 18.9 KB (18916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d1dd7704656f0e5abd80d84f159f32069f81c53535e48512db528dbc960be6`  
		Last Modified: Thu, 12 Feb 2026 21:06:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971f652d39303c7c4a6419fca4623de7099ac4b9e501ec606e3ee86bcc2d9ea7`  
		Last Modified: Thu, 12 Feb 2026 21:06:18 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92039b39faf7c57545fbacfc4daf7cf8305e91e70c447b862116d92415a15c3`  
		Last Modified: Thu, 12 Feb 2026 21:06:19 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:e7729993c65951e6d3cca0e69d79b68db4f5f6520b9ea1dda60b8b1372a8d2ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.9 KB (635919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e25a8130e1297a238cf761eba7df13b5b4b09adae2d447a05f0c94f762cb3e9`

```dockerfile
```

-	Layers:
	-	`sha256:9bfad529686f3ced1fc5c11d69e94c19d9f9fe4b6828fdec9a09ed3586063868`  
		Last Modified: Thu, 12 Feb 2026 21:06:17 GMT  
		Size: 596.3 KB (596293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f3538980cbad94229b338f4d9ea691db88129272287772e2eab0cfbe91fe19e`  
		Last Modified: Thu, 12 Feb 2026 21:06:17 GMT  
		Size: 39.6 KB (39626 bytes)  
		MIME: application/vnd.in-toto+json
