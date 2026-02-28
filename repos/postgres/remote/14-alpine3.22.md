## `postgres:14-alpine3.22`

```console
$ docker pull postgres@sha256:f3057001b96f2c44a4d0ba4fba3171895dbcededf7cac8a9a10b462ffe3ea9f5
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

### `postgres:14-alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:2118c921aa7eb345355d8205399bb61c184bed58e0210052c669d24e4cdb34b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108102290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c10ccda740e7de5a6c7480d56d7777c92f1d0f623cb0c113e173c8a825cb146`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:25:31 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:25:34 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:28:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:28:39 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:28:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:28:39 GMT
ENV PG_MAJOR=14
# Thu, 26 Feb 2026 19:28:39 GMT
ENV PG_VERSION=14.22
# Thu, 26 Feb 2026 19:28:39 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Thu, 26 Feb 2026 19:28:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:30:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:30:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:31:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:31:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:31:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:31:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:31:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:31:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:31:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:31:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:31:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:31:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fedd756505f7ace12e29c8ae189ca4b7f1be4e0dc5082014b18f1e4ec605207`  
		Last Modified: Thu, 26 Feb 2026 19:28:30 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c46d5bc900355f0b733ea3fb6760ba58720f3ecb57137778ff0dd2ff898a4c`  
		Last Modified: Thu, 26 Feb 2026 19:28:30 GMT  
		Size: 918.3 KB (918294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91adf0ce65d418f288eb17cab476ee9c93997efb14f5f7a42cfc6e26175e5a58`  
		Last Modified: Thu, 26 Feb 2026 19:31:15 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d9cf742ee86a4c072f823466596265073755081f70a45e7e1cbdf751f0d2d5`  
		Last Modified: Thu, 26 Feb 2026 19:31:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c416f88ef69f75e949ae58c6f08332beba4bc32e7d83adf659cb34d01d919ea2`  
		Last Modified: Thu, 26 Feb 2026 19:31:18 GMT  
		Size: 103.4 MB (103362334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7833046b25f220d2f6cbc6ddaf4c75e5000c288ba20355725d9bdbfc79387a`  
		Last Modified: Thu, 26 Feb 2026 19:31:16 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1119dfcc981e64217aa8db2b9e8d8a1d60a689bc0a8a2cabbce5bfee35ee8a61`  
		Last Modified: Thu, 26 Feb 2026 19:31:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d4c3501080762d76af404a2b8fe2438f9db948b03dbeceada5f77992778417`  
		Last Modified: Thu, 26 Feb 2026 19:31:17 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190039bcafeaf17e1ba8347b9d5832994fc79c91ef5484bf9a41006f7c29aa2b`  
		Last Modified: Thu, 26 Feb 2026 19:31:17 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee34520487a85872cb1590a9997894900927e0dbf82b4ef4eec39ebc2d9d3ffc`  
		Last Modified: Thu, 26 Feb 2026 19:31:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:55c8450a7299c3ab7f25a9916e4af690fe8e6ae24ca9fa3982d20133dc6c91c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.8 KB (639764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec4eb850e84f25990d808fda56e0b83199b8a175d59c1dbe8c95a5ec478b961`

```dockerfile
```

-	Layers:
	-	`sha256:c021d6997154a1b0a68a299711fc41412c0c60d2848521f9c326b9d446dc16b1`  
		Last Modified: Thu, 26 Feb 2026 19:31:16 GMT  
		Size: 596.3 KB (596315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30f26e0dea71c819ca57797fee4006d2405d378476cc4fea073077ec645abd98`  
		Last Modified: Thu, 26 Feb 2026 19:31:16 GMT  
		Size: 43.4 KB (43449 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:c2d93fd3bc3e50ae99cc7eb62dc9e14a0a2edb33fc9d71916d97b9e337a46bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87717575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d345aad360400f752eb414dc72d464f68f761ef00de975ea893f9908ac6d7538`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:28:36 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:28:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:28:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:28:40 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:28:40 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:28:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:28:40 GMT
ENV PG_MAJOR=14
# Thu, 26 Feb 2026 19:28:40 GMT
ENV PG_VERSION=14.22
# Thu, 26 Feb 2026 19:28:40 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Thu, 26 Feb 2026 19:28:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:31:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:31:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:31:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:31:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:31:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:31:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:31:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:31:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:31:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:31:20 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:31:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:31:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1f61211d6d276a701ca7917a13a70f6bdd1a2abffb2c920c59115a1e851d08`  
		Last Modified: Thu, 26 Feb 2026 19:31:30 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d4f8df4b3d0c617838aa9f87da510fa1d8bd7b926a3d8b6dc08783cd636913`  
		Last Modified: Thu, 26 Feb 2026 19:31:30 GMT  
		Size: 886.1 KB (886134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d7e7f79c31419f40a52c7973809a68489dcc0685e798ee5c168b7caba20433`  
		Last Modified: Thu, 26 Feb 2026 19:31:30 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd56bdb5063b249fd0f1a9067252e81f013051c207cadc6ddab3aba115787b9`  
		Last Modified: Thu, 26 Feb 2026 19:31:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34493ef0cc697991b910576abb13740ae55d8b20d0c71ebdf414ebeb51983779`  
		Last Modified: Thu, 26 Feb 2026 19:31:33 GMT  
		Size: 83.3 MB (83309614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d35df5ef3e213505bc59e7f9b6136437db3f519d978905ef85ff02aaeeb86c9`  
		Last Modified: Thu, 26 Feb 2026 19:31:31 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3920e2e8ffbd887cdccb780625a24aed6bb1db812b6231b56c067e1df298e25b`  
		Last Modified: Thu, 26 Feb 2026 19:31:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed86358852e9f2d7d77199cd3c01a1ef2b588d18841016a28daf8d07f611c79`  
		Last Modified: Thu, 26 Feb 2026 19:31:32 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1f49c604b474ba11c8c6d302341e0ec877b3fbaa805284113f8175ff4cade3`  
		Last Modified: Thu, 26 Feb 2026 19:31:32 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6ba26ad586c408392eada42efbf2a5eca4a94abb6df25ada1aafcd4dd5200b`  
		Last Modified: Thu, 26 Feb 2026 19:31:33 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:e26148e70307517623019adfae2dfdbf3386fbcdaf84099e3081e71008fbcadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 KB (43396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6d5a3208771becbe34ebcf2b9d0a0f985ffd28ab1581d9968bd1122db48d62`

```dockerfile
```

-	Layers:
	-	`sha256:e5ca46d53c94a9939da83438e0957e88bf4e69419d8cbb0f5e2474becb9fda01`  
		Last Modified: Thu, 26 Feb 2026 19:31:30 GMT  
		Size: 43.4 KB (43396 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:17318984e259d32893efba12e53210ecd146a2fa0507ed37475fceb7a168ae68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83024576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ee7f920903bb6d98ad1e8cc8940cc489dc49b9679922f37d2665a842fdb13b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:47:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:47:52 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:47:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:47:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:47:52 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:47:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:47:53 GMT
ENV PG_MAJOR=14
# Thu, 26 Feb 2026 19:47:53 GMT
ENV PG_VERSION=14.22
# Thu, 26 Feb 2026 19:47:53 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Thu, 26 Feb 2026 19:47:53 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:50:26 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:50:26 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:50:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:50:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:50:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:50:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:50:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:50:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:50:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:50:26 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:50:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:50:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4ae693826cfe220ee33febc0f6399965f7c200f2bfa0dfe30645ea08c4ee30`  
		Last Modified: Thu, 26 Feb 2026 19:50:37 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a5edef13fa19bd02cca5e86be83ca13f998fc8fbd0697315f28e26b3c990b6`  
		Last Modified: Thu, 26 Feb 2026 19:50:38 GMT  
		Size: 886.1 KB (886133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cded9f92021304906f3994e215b1093a74e8d3182808fbd1091603a5ab7cea6a`  
		Last Modified: Thu, 26 Feb 2026 19:50:37 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c068187b1b993b578695f076b4628145a8e9c8c10e76da10a9f63630037a637f`  
		Last Modified: Thu, 26 Feb 2026 19:50:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4101bf8a052c56d0c859ae18ac3dcdcfe057f8989addebd902ee3ba8b04cd2d7`  
		Last Modified: Thu, 26 Feb 2026 19:50:41 GMT  
		Size: 78.9 MB (78898024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080511b469708da3a611c21ec5c64914fd851379daf1fbe3d3120e0bb511958d`  
		Last Modified: Thu, 26 Feb 2026 19:50:39 GMT  
		Size: 9.2 KB (9208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081fe39ad85067fb83e37ff8ebe03138a176474f6fac266264e4806306ada405`  
		Last Modified: Thu, 26 Feb 2026 19:50:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b277b8b817d7342867e7f41068794af4430aca7a6639b2c2052ec2cc19a3d8e`  
		Last Modified: Thu, 26 Feb 2026 19:50:39 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d73ff23a2c862df8c01469395b9a5a6e118fc704dfcdf434fde83003e52b417`  
		Last Modified: Thu, 26 Feb 2026 19:50:40 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aad9aced4c35afabc6eb5b8d95534f46fc057d294cd4d5c97c583e605e2ecf8`  
		Last Modified: Thu, 26 Feb 2026 19:50:40 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:886ed9c0df59f85e3892aa63d864a879951ae8370d1b97d2a0ad2f9b97379dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.9 KB (639946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2185979dd00fb68be440f314daa3adf1bfc84f878c269bb03470c8173bc5872`

```dockerfile
```

-	Layers:
	-	`sha256:47d649637e8ea77fa0683ff437f891d053ab21fa01892e96fb416eccc9f4fbdd`  
		Last Modified: Thu, 26 Feb 2026 19:50:37 GMT  
		Size: 596.3 KB (596335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ff7fe7761ed9a457ef23f039a2b916458fabe437ca2af6739c5653210d8fa1`  
		Last Modified: Thu, 26 Feb 2026 19:50:37 GMT  
		Size: 43.6 KB (43611 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:fe712ac81e2659588a692f5a10d01866e02effae7f4fe29b1c3a371b43283010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104074691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a7220c3d5bb49915f8bf0c91ca04df455cc55774ab5947d662cef2d13c19de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:28:27 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:28:30 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:28:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:28:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:28:30 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:28:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:28:30 GMT
ENV PG_MAJOR=14
# Thu, 26 Feb 2026 19:28:30 GMT
ENV PG_VERSION=14.22
# Thu, 26 Feb 2026 19:28:30 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Thu, 26 Feb 2026 19:28:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:30:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:30:57 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:30:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:30:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:30:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:30:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:30:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:30:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:30:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:30:58 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:30:58 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:30:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852516660e9689c93a2b49730a0d8c3f376b81027051c3e1d7e3c556069d4341`  
		Last Modified: Thu, 26 Feb 2026 19:31:12 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d194ec99252ce0cad68eb5c9a4c8e1adcf40d60ab02c287b079766c64a6982`  
		Last Modified: Thu, 26 Feb 2026 19:31:12 GMT  
		Size: 873.5 KB (873486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14ef379c88032f95c8226dd21375e7bf7810f1a30b233b58ef6136d6239c41f`  
		Last Modified: Thu, 26 Feb 2026 19:31:12 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42910bba78f6f9308e38e6a46e35c7914ed04169f9a4bd862a0f04b3631fc4ec`  
		Last Modified: Thu, 26 Feb 2026 19:31:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9908505edd686d397dc7563acd2165885e44fe36e055e39951a9104dd260edc`  
		Last Modified: Thu, 26 Feb 2026 19:31:15 GMT  
		Size: 99.0 MB (99044905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcc0a3d5af38db1ebdb4f027a415b8e11b97728e6053e8d1de491524a27f050`  
		Last Modified: Thu, 26 Feb 2026 19:31:13 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d09077b22010caddb63ca517a78c58379e16568e7fe444a4d6c1cfbbb74cb42`  
		Last Modified: Thu, 26 Feb 2026 19:31:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b2cefb4cfc8cab899a7ebbbb80595c6fd2cd5f39a321eb422a68b41f4cf514`  
		Last Modified: Thu, 26 Feb 2026 19:31:13 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131265e2a16b1d008859c62b2e59bb3326d7cd4e882b9d641c9b17fce3c58742`  
		Last Modified: Thu, 26 Feb 2026 19:31:14 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ef009783061d3b93690605c50c0cf2381415d2d2c61baa35e4539d4d09fc2e`  
		Last Modified: Thu, 26 Feb 2026 19:31:14 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:1393e8728bdff2e0574a2ef5ee54a1d2cb2e55de061e7104fba1d6b1e01ec156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (639990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13ccd63cac813d5928a228b58ab6de150c290dcf1cb69d091000283eb1348fe`

```dockerfile
```

-	Layers:
	-	`sha256:572ca0daad438fc3ff36c56bd4248c5c8b8fc2bbf48ed4c422b6181fc32f1c8e`  
		Last Modified: Thu, 26 Feb 2026 19:31:12 GMT  
		Size: 596.3 KB (596347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45daf07cd1c7a340e56fb064482b5540260c7aa23b10160350b8269b0de48a02`  
		Last Modified: Thu, 26 Feb 2026 19:31:12 GMT  
		Size: 43.6 KB (43643 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:dbcf741654c9a9dfd17aea238492974183f68ef3b08e816399b62dea3507c8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114329287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cbebc02dd894816d1d6a97fd2cd149e9fb16a3010ad31ff34eb063ac36bd04f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:26:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:26:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:26:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:26:08 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:26:08 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:26:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:26:08 GMT
ENV PG_MAJOR=14
# Thu, 26 Feb 2026 19:26:08 GMT
ENV PG_VERSION=14.22
# Thu, 26 Feb 2026 19:26:08 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Thu, 26 Feb 2026 19:26:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:28:27 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:28:27 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:28:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:28:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:28:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:28:27 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:28:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:28:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:28:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:28:27 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:28:27 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:28:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cc70b6f4bc992658c0524b16e734a3b1097cdb1a7f35785a4a71135d2b4671`  
		Last Modified: Thu, 26 Feb 2026 19:28:43 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91786c06e26a9bec909c200a74a656ad4f8a3f197114f5d51b1ed8633ad9c363`  
		Last Modified: Thu, 26 Feb 2026 19:28:43 GMT  
		Size: 890.6 KB (890635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c23c325077a90622bf3d47cece22c13572a2bebb906db055a17adcee55a1ef`  
		Last Modified: Thu, 26 Feb 2026 19:28:43 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c5fd6c8c6f4abd8b1d6a99e45c47311e1dd58f70333674066f4d36652439e3`  
		Last Modified: Thu, 26 Feb 2026 19:28:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbfdea14160ac78e2517f9c418918514a9a37667ba9f510909cf83c522c7b6e`  
		Last Modified: Thu, 26 Feb 2026 19:28:47 GMT  
		Size: 109.8 MB (109801141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c41adea61a189760d68883664a3ff568546ca7bc207744f367afdddcf950640`  
		Last Modified: Thu, 26 Feb 2026 19:28:44 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f7d434bdb04ea733cf38eea87cca175f4a6b0ab56410536d03e042ef380f71`  
		Last Modified: Thu, 26 Feb 2026 19:28:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675c3ce79144ce42923a21c521245da9e4e469f923c5576d255d287cb5a8ed28`  
		Last Modified: Thu, 26 Feb 2026 19:28:44 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35a3aa952cae18fd1278229f1792c7248da0fee2d6a1bf0ac0b32018205f835`  
		Last Modified: Thu, 26 Feb 2026 19:28:45 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed273fc1dee7a69311cffd4ca2f473308989954062620e2d1d2969dca61c97c`  
		Last Modified: Thu, 26 Feb 2026 19:28:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:6628bf752ca112c896f9025dd8ad47e36e79eefc43ee843d5ce88d4ef64a113c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.7 KB (639711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6d95cc6cdb7756103fb280d3a6bceb1889caed430b2fc01c92d9cfee8637d6`

```dockerfile
```

-	Layers:
	-	`sha256:7a2ac95df9dd9e3dc5199aa6f1b3fb5b3dd9fc52771f9e7ae36401019b416a58`  
		Last Modified: Thu, 26 Feb 2026 19:28:43 GMT  
		Size: 596.3 KB (596300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7232dcdd11acc14108afba7e14665860df00d40128e888662a940855568d1123`  
		Last Modified: Thu, 26 Feb 2026 19:28:43 GMT  
		Size: 43.4 KB (43411 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:5ba3ef24dbc4f6e6148e591c3fa09cea79626f8f3d51d9c210ffda412f24723a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91802899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa11754504c36d575b5a2623866a9cf614c9218698e14ce4c9072be54295ac4a`
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
# Thu, 12 Feb 2026 21:20:55 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 12 Feb 2026 21:20:55 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:29:18 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:29:18 GMT
ENV PG_MAJOR=14
# Thu, 26 Feb 2026 19:29:18 GMT
ENV PG_VERSION=14.22
# Thu, 26 Feb 2026 19:29:18 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Thu, 26 Feb 2026 19:29:18 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:45:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:45:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:45:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:45:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:45:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:45:10 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:45:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:45:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:45:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:45:11 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:45:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:45:11 GMT
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
	-	`sha256:c7ad419382e4519d75f62994b2c5bec169e780789538a63d941296bcf7f49126`  
		Last Modified: Thu, 12 Feb 2026 21:25:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36e0ab2a77a2528ce4e52be54e629eb74605e6d15a1f6e99d8a45eb4c68b1a0`  
		Last Modified: Thu, 26 Feb 2026 19:33:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3db1edf0924ad24c2213fecdaa8c0a08ec613839527e9ac57f55076d2bf7a01`  
		Last Modified: Thu, 26 Feb 2026 19:45:40 GMT  
		Size: 87.2 MB (87172768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1123290111047deeddc531071dd995d8fbf10d93dc5192882c2f563db31ef8f4`  
		Last Modified: Thu, 26 Feb 2026 19:45:38 GMT  
		Size: 9.2 KB (9209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78948aa55956f0049128f559ff1296271c160801567f584d3e932a538ae22521`  
		Last Modified: Thu, 26 Feb 2026 19:45:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdc4e4061efc405b27b1ae6e3ec65e739a1ef0c39fddcbaca7529745b777f37`  
		Last Modified: Thu, 26 Feb 2026 19:45:38 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53992585d33f7d0e54f1bfa0f0a53a504ce9021329ffd4f78673ff1eb085651`  
		Last Modified: Thu, 26 Feb 2026 19:45:39 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3973d77cb2e3874c1969b69e8f7f41115d3b9abcc7d6e250186dcc622cf87d1d`  
		Last Modified: Thu, 26 Feb 2026 19:45:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:00f033e41a14100a29ab8a136b94140d07075b02c5a13a4fd18f97c99eb6e439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.2 KB (636215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80ab738495993c9345504c707a8f744ad01df6434333bf0cfae7724a5c8331c`

```dockerfile
```

-	Layers:
	-	`sha256:5a56d9c8089fa0dd9f973090fcf1e63e5c37255170bb3721da3a5b1ca127b46e`  
		Last Modified: Thu, 26 Feb 2026 19:45:38 GMT  
		Size: 592.7 KB (592724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b464824bd4b68cd32de953091fed3b1db360ad1a7a0a19bdada58cb139fa10a3`  
		Last Modified: Thu, 26 Feb 2026 19:45:38 GMT  
		Size: 43.5 KB (43491 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:5e3dd5cef66b32de7d717224b54e993e3bcc3df11451b59345c20b64c7296199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.0 MB (107958438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b615ec26a0fdf7cf5d0a262e36e8adc8b301351db2d82fe5536c87e9790752eb`
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
# Fri, 13 Feb 2026 08:02:34 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 13 Feb 2026 08:02:34 GMT
ENV LANG=en_US.utf8
# Sat, 28 Feb 2026 10:59:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 28 Feb 2026 10:59:41 GMT
ENV PG_MAJOR=14
# Sat, 28 Feb 2026 10:59:41 GMT
ENV PG_VERSION=14.22
# Sat, 28 Feb 2026 10:59:41 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Sat, 28 Feb 2026 10:59:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 28 Feb 2026 15:24:36 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 28 Feb 2026 15:24:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 28 Feb 2026 15:24:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 28 Feb 2026 15:24:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 28 Feb 2026 15:24:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sat, 28 Feb 2026 15:24:38 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 28 Feb 2026 15:24:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 15:24:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 28 Feb 2026 15:24:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 15:24:38 GMT
STOPSIGNAL SIGINT
# Sat, 28 Feb 2026 15:24:38 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 28 Feb 2026 15:24:38 GMT
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
	-	`sha256:1fefaa019570f036a479949adc1cff90d83d62dfcccda924ecbc9fb276d79751`  
		Last Modified: Fri, 13 Feb 2026 08:54:08 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a21a3b98c9b6bafb53cc153f92fb4167f502f246a409bab23715b2cfca06be`  
		Last Modified: Sat, 28 Feb 2026 11:51:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e812e1dccd98e1a48eb6760f37f0de08ff5e05c77e9bd68957d8b56b9ab88ac6`  
		Last Modified: Sat, 28 Feb 2026 15:27:42 GMT  
		Size: 103.6 MB (103557581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f49b2cf6bdc073a2d19d75010b617466870c4561727096f48c874e3511257`  
		Last Modified: Sat, 28 Feb 2026 15:27:27 GMT  
		Size: 9.2 KB (9210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb56090122314f41b7414e92d9ebe6efebf65cbe0a2b4cea7053caa92ed007dc`  
		Last Modified: Sat, 28 Feb 2026 15:27:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e568185d9d03439d4c982be1d13b97398d00493b5c9138bf7a558aeeafad8f4f`  
		Last Modified: Sat, 28 Feb 2026 15:27:27 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172b3ed13e2090f9f81c63b226ce621a88dc096f1909ebf6c6e33f63b0bb4071`  
		Last Modified: Sat, 28 Feb 2026 15:27:28 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fd8cfa1bb08fa7db72225a802a035a6901c78619c93db96dec0c1a4d3a93f4`  
		Last Modified: Sat, 28 Feb 2026 15:27:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:721d0c0a6793fbdc5c945968f1cff11d6d5321f751d1056db962053d7adf2e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.9 KB (637879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e90580bd61c66f5ed073f82447cc64c85158c4ba09627fbaf0dad3bd607d05`

```dockerfile
```

-	Layers:
	-	`sha256:68cf1e0edc15330ad8859f5054aa9a154c9a122741c1b98756afae24aca669b2`  
		Last Modified: Sat, 28 Feb 2026 15:27:27 GMT  
		Size: 594.4 KB (594382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3b12c1a1c3a9021c106661d99b72d6504c3f5e6587c26c0cde3bb1934a34138`  
		Last Modified: Sat, 28 Feb 2026 15:27:27 GMT  
		Size: 43.5 KB (43497 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:4b6791499598d82c0a7142d6e16f379b444a172b7619df46326f3dd754576ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116774302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0fff60bf83dfe7127ffc39d6f426f36529cd8596e4ffb194614451a72966e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:14:50 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:14:56 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:14:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:59:44 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:59:44 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:59:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:59:44 GMT
ENV PG_MAJOR=14
# Thu, 26 Feb 2026 19:59:44 GMT
ENV PG_VERSION=14.22
# Thu, 26 Feb 2026 19:59:44 GMT
ENV PG_SHA256=f57938ad30067077720277f6d7db05aafc07d1545efd2ed82f199ba828a7ad34
# Thu, 26 Feb 2026 19:59:44 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 20:10:00 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 20:10:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 20:10:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 20:10:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 20:10:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 20:10:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 20:10:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 20:10:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 20:10:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 20:10:02 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 20:10:02 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 20:10:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c67cc230b3dd7b560fa1987c9d84e3183b632f12d48ce939c5c92b1ccb3f06`  
		Last Modified: Thu, 26 Feb 2026 19:19:31 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fea80e1df1f3240aa5c657b48535279b84e09b47913351236b888b90c60dcaa`  
		Last Modified: Thu, 26 Feb 2026 19:19:32 GMT  
		Size: 894.4 KB (894422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dbc0a8dc57dbf8a6f6ee7d5b609acc6dffb0433686ba4272a36b621a1f2580`  
		Last Modified: Thu, 26 Feb 2026 20:04:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716e75b99f1fa230bc7600aa864ad7a2ad43a294ae5b7281a6b60f1e04882c32`  
		Last Modified: Thu, 26 Feb 2026 20:04:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ab86f99f37994c0dd7494020a6594c77a792e8ca0b2ff1dd3c81eead9468fd`  
		Last Modified: Thu, 26 Feb 2026 20:10:37 GMT  
		Size: 112.2 MB (112212658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc4d4d80a1ec135b8d34d2e47c422b1036b13cb64e8f372c25172832c952233`  
		Last Modified: Thu, 26 Feb 2026 20:10:33 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f180e2e22b171ed042d80c9745ddf11a2863b97b5d76ea2bc2213f1a9256bb`  
		Last Modified: Thu, 26 Feb 2026 20:10:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3042c04f158a373504cf5223aadcfc3ccbab37b2ade6d340b97407d54a574a`  
		Last Modified: Thu, 26 Feb 2026 20:10:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde49e954417f8d6b3d2cf6c75a224dc2fe845e049502976e5a7d20352dd0621`  
		Last Modified: Thu, 26 Feb 2026 20:10:34 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cf936bdd606b98e16ec683a7ff8d91fa641c9a55d5fe752be96bb539f1ebd6`  
		Last Modified: Thu, 26 Feb 2026 20:10:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:4aebf2302f408547ca7733070926047387a8f5798fb474868a9adf93dddbef29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 KB (637812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac04671e6225ae2a1f1dc931f771a8ee2d5ffb68f98de9d09f56cab1145aff5e`

```dockerfile
```

-	Layers:
	-	`sha256:6450e018701de039731aaa50948a2911c84fb3a0f5009ddd3310e521bd22f507`  
		Last Modified: Thu, 26 Feb 2026 20:10:33 GMT  
		Size: 594.4 KB (594364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b8c7d688bfd9e847c2480ce721a56dce49ddf7076d99dc947ac73c7f08e2d80`  
		Last Modified: Thu, 26 Feb 2026 20:10:33 GMT  
		Size: 43.4 KB (43448 bytes)  
		MIME: application/vnd.in-toto+json
