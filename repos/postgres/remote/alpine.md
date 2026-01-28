## `postgres:alpine`

```console
$ docker pull postgres@sha256:bff147924b5492716cb1439f1949e7c8f42ccdd628af4f66415e31212ebdc462
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

### `postgres:alpine` - linux; amd64

```console
$ docker pull postgres@sha256:e1c9df090b0f98e599812b495c8677af65da059b12953de6857c0684510409e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.0 MB (111953794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425cb9783656f2a5b608655f0c841b37c1d87a6df2f816d2a2cb1a548eab7676`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:29:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:29:08 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:29:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:29:08 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:29:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:29:08 GMT
ENV PG_MAJOR=18
# Wed, 28 Jan 2026 02:29:08 GMT
ENV PG_VERSION=18.1
# Wed, 28 Jan 2026 02:29:08 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Wed, 28 Jan 2026 02:29:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:31:27 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:31:27 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:31:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:31:27 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 28 Jan 2026 02:31:27 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Wed, 28 Jan 2026 02:31:27 GMT
VOLUME [/var/lib/postgresql]
# Wed, 28 Jan 2026 02:31:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:31:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:31:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:31:27 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:31:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:31:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34bdd99dc3a0d2ea059297d16ed4ca65e179fd7f3b74a2906f066618d8597c6`  
		Last Modified: Wed, 28 Jan 2026 02:31:42 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96616cf7541b8d8ffad9f7e26cc5d4495496a7836d443794d659e3e0658a81c9`  
		Last Modified: Wed, 28 Jan 2026 02:31:42 GMT  
		Size: 922.9 KB (922911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c030b5eea758f49cbd898b3baa47b4cb353ce6c720f5071dda8f19864d14fd65`  
		Last Modified: Wed, 28 Jan 2026 02:31:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724b010f73c7871b1af6a11da8bbc5801785d3e0ff8e13e52da9b8193d500b84`  
		Last Modified: Wed, 28 Jan 2026 02:31:45 GMT  
		Size: 107.1 MB (107142863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006c1776dd70551af804ec4de65035986e2775e9881c21dcd2fc0efd6571bcfa`  
		Last Modified: Wed, 28 Jan 2026 02:31:43 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c63fc4482dce1b8f6b29aa3f451d7943c9631d6dcb02ef02e9d1408b1b898b`  
		Last Modified: Wed, 28 Jan 2026 02:31:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973f7ff6bf5c14c3b2dc8e8f35dd89cc2540142f6875e5e4c1ae2b84562478d`  
		Last Modified: Wed, 28 Jan 2026 02:31:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab61e97249e7d4d89a2abc51473046015ce857ec515fc475c536f8cbf92efc4`  
		Last Modified: Wed, 28 Jan 2026 02:31:44 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf46f2864ac96dc23823d0d431a1a71a0df74f29177251e433b7877abaa05aa`  
		Last Modified: Wed, 28 Jan 2026 02:31:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:eb7a69c231a155331f1beae001eb9337efb8fa2bdcf08f09ab9f335e15a51dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.4 KB (643424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcb97bbaef211475fe907eb4d764bf1d102cf93fc4793347493b45454d09c28`

```dockerfile
```

-	Layers:
	-	`sha256:24ef33f670cea2c2dbb85300ef128276b239f3f34385ae2b8ba47899d7582eed`  
		Last Modified: Wed, 28 Jan 2026 02:31:42 GMT  
		Size: 600.3 KB (600312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a332fea194caf66602c51a2d9de64495d10c5311180cf351a4f00e6631085822`  
		Last Modified: Wed, 28 Jan 2026 02:31:42 GMT  
		Size: 43.1 KB (43112 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:70be7607da70693096a6f80f2a8a657ee3699aaf4c793c5d1248899441e9deea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91421424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8d76c86a3578e00d2982da0b176a64e67ee1e0ddeca361e401d68a282cc746`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:44:42 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 00:44:46 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 00:44:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 00:44:46 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 00:44:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 00:44:46 GMT
ENV PG_MAJOR=18
# Thu, 18 Dec 2025 00:44:46 GMT
ENV PG_VERSION=18.1
# Thu, 18 Dec 2025 00:44:46 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 18 Dec 2025 00:44:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 00:47:36 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 00:47:36 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 00:47:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 00:47:36 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 18 Dec 2025 00:47:36 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 18 Dec 2025 00:47:36 GMT
VOLUME [/var/lib/postgresql]
# Thu, 18 Dec 2025 00:47:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:47:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 00:47:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:47:36 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 00:47:36 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 00:47:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb1338ad38fbe457cff0eef9964a724acbbfdd43caabfee8cf29eb3459e7998`  
		Last Modified: Thu, 18 Dec 2025 00:47:47 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b194cda91b6a94af3348c878e9f25b3303e5f2af8d17d7111e4ed1346610e0`  
		Last Modified: Thu, 18 Dec 2025 00:47:47 GMT  
		Size: 889.5 KB (889470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd29e571df216763b8a9a7b405cea0b6ef7cc3071aa22381872451f65380ae5`  
		Last Modified: Thu, 18 Dec 2025 00:47:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a222b473aaae4595e3d4638d698c0cf904872d3928f381bf9f1e90db0b89b127`  
		Last Modified: Thu, 18 Dec 2025 00:47:49 GMT  
		Size: 86.9 MB (86937332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe68d020bfe136bbfa8c6c07fa218cfe743dabbc2771e4a52a7c9eb9945b876`  
		Last Modified: Thu, 18 Dec 2025 00:47:48 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496e35e55459e3559d9927de770dfacd1004876415a20ab8ca6a9541af86767a`  
		Last Modified: Thu, 18 Dec 2025 00:47:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da3f4ef29cac882b9b908db8d69438188cdc2a84fb668a3aebb89d844484e5a`  
		Last Modified: Thu, 18 Dec 2025 00:47:49 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8bc6043a09873ea8818706b03ce04b9c30bfcc062a7d9fd0670046602f0b0b`  
		Last Modified: Thu, 18 Dec 2025 00:47:49 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e1633f37e841b99445bad01eb59578e2c5a665a7e75d20762ee13e8b6bb2b8`  
		Last Modified: Thu, 18 Dec 2025 00:47:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:052fffe21ebece353fd7f6db27acb0947a3a96eba0d45b78d636da61c5098087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 KB (43076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185af0be490abb544c28d1a97b9e63e9ca10b577aa969233d774b7696326928f`

```dockerfile
```

-	Layers:
	-	`sha256:852e5f454cd513db1dcad574a7ddb86b11bb982184270410b8074b8ad9d9a8bf`  
		Last Modified: Thu, 18 Dec 2025 00:47:47 GMT  
		Size: 43.1 KB (43076 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:fb6c708da36da2ac42a35d8d0ac3d788cc8e6620430722bb136dbe31ada5914f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86574013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163d5a18575abec40753f88f529ef73fafc6888b9e7fec2a70ce26cea3438bb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:43:02 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:43:06 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:43:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:43:06 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:43:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:43:06 GMT
ENV PG_MAJOR=18
# Wed, 28 Jan 2026 02:43:06 GMT
ENV PG_VERSION=18.1
# Wed, 28 Jan 2026 02:43:06 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Wed, 28 Jan 2026 02:43:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:47:53 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:47:53 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:47:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:47:53 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 28 Jan 2026 02:47:53 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Wed, 28 Jan 2026 02:47:53 GMT
VOLUME [/var/lib/postgresql]
# Wed, 28 Jan 2026 02:47:53 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:47:53 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:47:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:47:53 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:47:53 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:47:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707c9fe3e004fa3dea6cd5c66a94cb9c84758a5c6faa02076f1672acf49372d2`  
		Last Modified: Wed, 28 Jan 2026 02:48:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9412493db081a065b617622c8fe037a71968ed9dd99323ffe4bed3d9e3e684af`  
		Last Modified: Wed, 28 Jan 2026 02:48:05 GMT  
		Size: 889.5 KB (889503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75c138e77c979c72b868015b5413332ffbe793a1ef2f0a3bf17249df8f1e5ba`  
		Last Modified: Wed, 28 Jan 2026 02:48:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de58fbb4a389f259f0493cc2d5de5d5587326651f7f2a3dc4fb34551fd27de5`  
		Last Modified: Wed, 28 Jan 2026 02:48:07 GMT  
		Size: 82.4 MB (82376591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46911296d3e8620ae069ec2fcdd3aceb0ccf930dac92f348c966255d824542bd`  
		Last Modified: Wed, 28 Jan 2026 02:48:06 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6835a1ce07f8f47ae6f5fe64925d749d562cdf8efec9649642a6ffd896eab117`  
		Last Modified: Wed, 28 Jan 2026 02:48:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d7c43145d3cd6b4558ad9ce2abe35352fbce4481cddeb511f4f2930c493ccc`  
		Last Modified: Wed, 28 Jan 2026 02:48:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0636a48d0003c336a73da199b0abf7dcc5ee5f2cbd6bf4bf19f0196ab090223e`  
		Last Modified: Wed, 28 Jan 2026 02:48:07 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b54d98a6ec3f47d7d05ac6f648afc295d7c2dd5ec6219970528a38a7ba62b1`  
		Last Modified: Wed, 28 Jan 2026 02:48:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:6acb836ef94fe4d40ffdfd04c694e9da80b9ad9c497b74fe04b7f4079a5cd8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.0 KB (643007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6261dae6f48410821f9088f3f63199d709bfa82a10434218eefa42ecb93d89cf`

```dockerfile
```

-	Layers:
	-	`sha256:694169dcfc4a540f54a845bdbb4b816ebd6281e5f217c27543194294f01a184d`  
		Last Modified: Wed, 28 Jan 2026 02:48:05 GMT  
		Size: 599.7 KB (599714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80d76e0435710c05572f0f026e93fca8f7a9670235004c14e63775351107629b`  
		Last Modified: Wed, 28 Jan 2026 02:48:05 GMT  
		Size: 43.3 KB (43293 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:c81adf6d3c1c1efcae6b48418b0c9f634f0f3dc54cf567fdb6206b64d8d5023a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110133584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f15063057c4c53a2f069d39d95fe466c1ab89458611acdc6d079414e6094256`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:30:57 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:31:00 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:31:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:31:00 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:31:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:31:00 GMT
ENV PG_MAJOR=18
# Wed, 28 Jan 2026 02:31:00 GMT
ENV PG_VERSION=18.1
# Wed, 28 Jan 2026 02:31:00 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Wed, 28 Jan 2026 02:31:00 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:33:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:33:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:33:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:33:25 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 28 Jan 2026 02:33:25 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Wed, 28 Jan 2026 02:33:25 GMT
VOLUME [/var/lib/postgresql]
# Wed, 28 Jan 2026 02:33:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:33:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:33:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:33:26 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:33:26 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:33:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d020684c22478cdecffeab38e2312511ad9ac9bce371233074bbe9df4c72ab0`  
		Last Modified: Wed, 28 Jan 2026 02:33:41 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0dac0a9ca7c4f09afb97c1770621e40d4a2b5cad851fd07d4da05cf9e76ba06`  
		Last Modified: Wed, 28 Jan 2026 02:33:41 GMT  
		Size: 876.5 KB (876489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa8d7db09d5194c22d7c76d3ef3abc8ebaac86e2ee1c7a2eb4213846829a2d8`  
		Last Modified: Wed, 28 Jan 2026 02:33:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3265c1d138f0db35f97c15e647ff9e35fec0bbb0036217ddb2d77a7ad0f80d74`  
		Last Modified: Wed, 28 Jan 2026 02:33:44 GMT  
		Size: 105.0 MB (105033807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f83838420696d257f558fe090863b98685518f78267f482a55d5dca51f98e80`  
		Last Modified: Wed, 28 Jan 2026 02:33:42 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e31cac0486b0c9652815e9537a37c7925deeb1e2191ee71b59b855b5ab3814`  
		Last Modified: Wed, 28 Jan 2026 02:33:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1718d632d2b9d322c85d692236677293aa3322f396aa7546ff53ca0bf673b11a`  
		Last Modified: Wed, 28 Jan 2026 02:33:42 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d463307ee8fad97ab78cb9addd8e446904287162e2327663df7753d2f5dfd93`  
		Last Modified: Wed, 28 Jan 2026 02:33:43 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39db2fe67eb5a37953b91a65456bba517061be99e34af238c8db1a4f1c71eac6`  
		Last Modified: Wed, 28 Jan 2026 02:33:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:3d6ea8e17e9a6d80dd8bab33744a741ec62eb23d46eee891563bf70c440cda85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.1 KB (643087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9657759b64498608db6b6f387ad15dfdfdba11192f4c448d7ada98b46f5067fb`

```dockerfile
```

-	Layers:
	-	`sha256:3ab5ccd3d8e70e5fd5b32cf2f4bb40e5791b21e190da705447be02edeb7266f8`  
		Last Modified: Wed, 28 Jan 2026 02:33:41 GMT  
		Size: 599.7 KB (599742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be28267c4a6f08dc335c4d14a3d227197036625c8911b4d233f3ee8be340e407`  
		Last Modified: Wed, 28 Jan 2026 02:33:41 GMT  
		Size: 43.3 KB (43345 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine` - linux; 386

```console
$ docker pull postgres@sha256:5edabbf7ddfea8ee78faef3d9e7091a51e8fe4d6655f2e131dbf5ab03a43a99a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118114563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ec81a76e4fd7dc00e22a357922c3dd8a6dac67736295fc7749acb42066d75f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:25:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 02:25:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 02:25:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 02:25:47 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 02:25:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 02:25:47 GMT
ENV PG_MAJOR=18
# Wed, 28 Jan 2026 02:25:47 GMT
ENV PG_VERSION=18.1
# Wed, 28 Jan 2026 02:25:47 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Wed, 28 Jan 2026 02:25:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 02:28:27 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 02:28:27 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 02:28:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 02:28:27 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 28 Jan 2026 02:28:27 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Wed, 28 Jan 2026 02:28:27 GMT
VOLUME [/var/lib/postgresql]
# Wed, 28 Jan 2026 02:28:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:28:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 02:28:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:28:27 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 02:28:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 02:28:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ef6a41eacad71a09189571c623ffff9a7d829af61e781fa78fcc661de0f035`  
		Last Modified: Wed, 28 Jan 2026 02:28:42 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c4c6c77c38b7152fab4d1018ba2e497b4b51a75c3a558816faad6c1bd420d8`  
		Last Modified: Wed, 28 Jan 2026 02:28:42 GMT  
		Size: 893.3 KB (893252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba65eb7335c10cb39b1f6eee04c98e91099814d2af3ac7c7847b4bad38ed8802`  
		Last Modified: Wed, 28 Jan 2026 02:28:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa674befce45a8d215ffd559d40e0820cd2589471a288505d2ae92f69de9a323`  
		Last Modified: Wed, 28 Jan 2026 02:28:45 GMT  
		Size: 113.5 MB (113508116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930104454c6dccd287f7e2bde3c3cf5d17235e1ac0d3ca131882a4a0f9daffb8`  
		Last Modified: Wed, 28 Jan 2026 02:28:43 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03433b2a8dbaea9187b16f5c9c803be86e07e50a269a247e591959b278815a95`  
		Last Modified: Wed, 28 Jan 2026 02:28:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5d441a9ef97e7e01e62feacfe8eb2fbc5c7e16cb5eb38c54be2948a57cd30`  
		Last Modified: Wed, 28 Jan 2026 02:28:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ca410b365ce8ce37f94d393e53462ba09462b0be8a50de1bea21f2c68a98d2`  
		Last Modified: Wed, 28 Jan 2026 02:28:44 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51fc24c9d66c4877f8970359d044b0feb10e1290edbbd9be45de86d7f6c31a8`  
		Last Modified: Wed, 28 Jan 2026 02:28:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:2d4e3437c5f0b0acc0ecf90138b7bde739bff774320582c3591f42fcee7a69a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.3 KB (643333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bfc777a719b343f77a40629510f7044c98db2044aee8f8695692626f957cc23`

```dockerfile
```

-	Layers:
	-	`sha256:3d35a59b887d2dee419e4f8ed43bcbde7ac1ddb5bae2bf166938fc4fed396eda`  
		Last Modified: Wed, 28 Jan 2026 02:28:42 GMT  
		Size: 600.3 KB (600277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6279175c082416714505f18247efcfc936a0c0b25f0920e27876399e141191e0`  
		Last Modified: Wed, 28 Jan 2026 02:28:42 GMT  
		Size: 43.1 KB (43056 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:10eaadf9270f899d1bd2c30d69ca337e61195d8fe9253666b51562eb7a72fe5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97053571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5325cfab163f505cffa0a5b70ed9adadb45a3cd94b50cf1c5b448c1d26451aef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:31:57 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 28 Jan 2026 03:32:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 28 Jan 2026 03:32:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Jan 2026 03:32:03 GMT
ENV LANG=en_US.utf8
# Wed, 28 Jan 2026 03:32:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Jan 2026 03:32:03 GMT
ENV PG_MAJOR=18
# Wed, 28 Jan 2026 03:32:03 GMT
ENV PG_VERSION=18.1
# Wed, 28 Jan 2026 03:32:03 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Wed, 28 Jan 2026 03:32:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 28 Jan 2026 03:34:43 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 28 Jan 2026 03:34:44 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 28 Jan 2026 03:34:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 28 Jan 2026 03:34:44 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 28 Jan 2026 03:34:44 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Wed, 28 Jan 2026 03:34:44 GMT
VOLUME [/var/lib/postgresql]
# Wed, 28 Jan 2026 03:34:45 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:34:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 28 Jan 2026 03:34:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 03:34:45 GMT
STOPSIGNAL SIGINT
# Wed, 28 Jan 2026 03:34:45 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 28 Jan 2026 03:34:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd4e647df17c82db9ca398b2f463b9b25ee74420a55b31a9516facb1afa9c46`  
		Last Modified: Wed, 28 Jan 2026 03:35:18 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71de422e36f20b27957805987c70f9baf3d78aeb5185cefb6ba5e8f87a61453`  
		Last Modified: Wed, 28 Jan 2026 03:35:19 GMT  
		Size: 881.5 KB (881539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7649bce93f6f6f2482a38dc7082290155239a95f5f9f1e205d69594e44341386`  
		Last Modified: Wed, 28 Jan 2026 03:35:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f900a7baf6eac79f5c90f10696279190ae9b15a955a40f2c5c807e0caeea7f9`  
		Last Modified: Wed, 28 Jan 2026 03:35:21 GMT  
		Size: 92.3 MB (92316178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2705587bad70461e86cbfe439f16d82d433d196df2734a4eae9e44f1562965`  
		Last Modified: Wed, 28 Jan 2026 03:35:20 GMT  
		Size: 18.8 KB (18784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ff2c826717172b086ab7d5e4fd1196e8fc91f8ed526eab7f23970158ed944c`  
		Last Modified: Wed, 28 Jan 2026 03:35:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12eddb8406cfdb2f47b5eaa800b3cbe3b9ba3efed9148bd9048d16b0e3aee64e`  
		Last Modified: Wed, 28 Jan 2026 03:35:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69d5a6053d783231af120f49134c564008d1077a1b3df9c1c3e7a1cbf4d5600`  
		Last Modified: Wed, 28 Jan 2026 03:35:21 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbcbf84ae0c2dc8968f938683e21da0da1dacdad26dae9fc4c6e126a3b57bad`  
		Last Modified: Wed, 28 Jan 2026 03:35:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:a42dbb3697c4dc8d51796ad7d10e340ce41cbc130e3faca65344b58e5eedded3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.2 KB (641221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b843eddf1376cdd7862b6e3835f3afc507f461848cd08ae3853f2ed882f8be`

```dockerfile
```

-	Layers:
	-	`sha256:72691eb5c4e9ca75e75d971f120b8813eed12b1633c712d4fee24ffc9db6883a`  
		Last Modified: Wed, 28 Jan 2026 03:35:19 GMT  
		Size: 598.0 KB (598045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f53553dadd897dcb9f83454c6b795c8f59034389e71528f4ecb1eb8a0553ce0`  
		Last Modified: Wed, 28 Jan 2026 03:35:19 GMT  
		Size: 43.2 KB (43176 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:0bdf47bd7a6be5c2805df68ca0489d9c9cfeee1b7bc228b977109b16b4d8bfaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113209112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650b60de93541fc796472df7ed3059e337252ea5de860e5848d0c8d15ec5e4d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 22:58:49 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 22:59:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 22:59:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 22:59:01 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 22:59:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 22:59:01 GMT
ENV PG_MAJOR=18
# Thu, 18 Dec 2025 22:59:01 GMT
ENV PG_VERSION=18.1
# Thu, 18 Dec 2025 22:59:01 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 18 Dec 2025 22:59:01 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 23:49:10 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 23:49:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 23:49:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 23:49:11 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 18 Dec 2025 23:49:12 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 18 Dec 2025 23:49:12 GMT
VOLUME [/var/lib/postgresql]
# Thu, 18 Dec 2025 23:49:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 23:49:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 23:49:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 23:49:12 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 23:49:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 23:49:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e7504fb8b5ca902553810400e8ecf856a5984c36fb7dba7b9d1932f5432750`  
		Last Modified: Thu, 18 Dec 2025 23:52:05 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254154902548782aac7bbe74d12c713d81df39d8b697e905a7ada02053473207`  
		Last Modified: Thu, 18 Dec 2025 23:52:05 GMT  
		Size: 868.9 KB (868948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cb1e707cecbd8b342e8230a81de52b30274d906375bb62c7f6fa905a968ed1`  
		Last Modified: Thu, 18 Dec 2025 23:52:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0565a4b439268fc9d13bb8f0cbe4d925176671b7731ba0d964103b1b8dfca1de`  
		Last Modified: Thu, 18 Dec 2025 23:52:21 GMT  
		Size: 108.7 MB (108730019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbdff487f9f4ca85731291693e74c6626d7b0f07b325a2556057d4ee24896d0`  
		Last Modified: Thu, 18 Dec 2025 23:52:06 GMT  
		Size: 18.8 KB (18782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f6d1b4ee56c2634692a6ca09d95e010948a557484ec289faef583f345d247c`  
		Last Modified: Thu, 18 Dec 2025 23:52:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7345f722ce181178c558639a5ee02fadd1a2551c33faa547bc1066a8255c08a5`  
		Last Modified: Thu, 18 Dec 2025 23:52:07 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ab73ca0341f968b230e90e80bfa2ff3bc02c495b592b4c8f4e2e21e0ee8b9e`  
		Last Modified: Thu, 18 Dec 2025 23:52:08 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed8dba0ce3ae49a6ff138fb10890e85634942b811fdd02dc9ce05ded80f0970`  
		Last Modified: Thu, 18 Dec 2025 23:52:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:d9ee63e2375873a7a3befa779f1fb78283e98a425ab504fd4d0e96bbe7ea6f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.9 KB (642885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38c1a66b46eb565ff8b35e874fd801640c499ca952f07876dcd4c719ff9733a`

```dockerfile
```

-	Layers:
	-	`sha256:6ae7ccbea223d2ec724898f87fd63f6c86285bac9403d6c9e7b1c1cf48d7b8c2`  
		Last Modified: Thu, 18 Dec 2025 23:52:05 GMT  
		Size: 599.7 KB (599703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a76e1cf95eddb207c4ab24210a0ff8bb2f9816124bdc5a10e01c57ba459325a3`  
		Last Modified: Thu, 18 Dec 2025 23:52:05 GMT  
		Size: 43.2 KB (43182 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine` - linux; s390x

```console
$ docker pull postgres@sha256:ec749c084f1c568b4edf66301f0ea30f65186427a1cbdd8c2aac66a961baa911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120177082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e2d03da4657087c943fed4334fba57a43c50b5520282436b280f19af7d2cc1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:06:27 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 18 Dec 2025 01:06:32 GMT
ENV GOSU_VERSION=1.19
# Thu, 18 Dec 2025 01:06:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Dec 2025 01:06:32 GMT
ENV LANG=en_US.utf8
# Thu, 18 Dec 2025 01:06:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Dec 2025 01:06:32 GMT
ENV PG_MAJOR=18
# Thu, 18 Dec 2025 01:06:32 GMT
ENV PG_VERSION=18.1
# Thu, 18 Dec 2025 01:06:32 GMT
ENV PG_SHA256=ff86675c336c46e98ac991ebb306d1b67621ece1d06787beaade312c2c915d54
# Thu, 18 Dec 2025 01:06:32 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 18 Dec 2025 01:11:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 18 Dec 2025 01:11:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 18 Dec 2025 01:11:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 18 Dec 2025 01:11:41 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 18 Dec 2025 01:11:41 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 18 Dec 2025 01:11:41 GMT
VOLUME [/var/lib/postgresql]
# Thu, 18 Dec 2025 01:11:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:11:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 18 Dec 2025 01:11:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 01:11:41 GMT
STOPSIGNAL SIGINT
# Thu, 18 Dec 2025 01:11:41 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 18 Dec 2025 01:11:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:04 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c5f2050f07a5cb01bb74eff322320d79ef052693ec1bf2e791c3e34ee9ad2`  
		Last Modified: Thu, 18 Dec 2025 01:12:14 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3d39d8e02436f0b019f16e16fc19ff6b779eae84772469808fc5da728fdd6f`  
		Last Modified: Thu, 18 Dec 2025 01:12:14 GMT  
		Size: 897.4 KB (897417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6bb97427b6f31c3b22f870e9da44ec7674b38e9d345bdba0e657a54306f4a7`  
		Last Modified: Thu, 18 Dec 2025 01:12:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c9e342b22362c6025ced5450bf4ef1db32b6a57196ae9c4da1a481308b3abe`  
		Last Modified: Thu, 18 Dec 2025 01:12:20 GMT  
		Size: 115.5 MB (115529157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32abf35c4794f0ad4046c13a6d81222336c7f6b84ffcda9ff3f3580d4b8bd4ec`  
		Last Modified: Thu, 18 Dec 2025 01:12:17 GMT  
		Size: 18.8 KB (18776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea32e6e41a70802fc40ae0a5831e0c8af2fe921814a6ad20d120407ce280a74`  
		Last Modified: Thu, 18 Dec 2025 01:12:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4cd53776f3ca695a415c1a469b846d85b09974ac5eae0761b5246d97827f53`  
		Last Modified: Thu, 18 Dec 2025 01:12:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e24d1b441790c16493c7ba2b2d9a0873fe1cbce70ddce85dca7e2647315aee`  
		Last Modified: Thu, 18 Dec 2025 01:12:18 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f79bc4ac9c5a067e1355a580d75b99cd28982844bf10d0ad512f6a3af10697`  
		Last Modified: Thu, 18 Dec 2025 01:12:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:e366401797406e758720eca2a08ee15d3eb470f915ab646ed4052c3616c6a43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.8 KB (642773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa2f32469d1287d2e2cc94a6c18bda3d0e3ce92d6210ac67804e3c196ad28c2`

```dockerfile
```

-	Layers:
	-	`sha256:c46d528b16a89a45d7be24a9d9fc2479bf9e4bde86bb6a59e7589c42bac39b3b`  
		Last Modified: Thu, 18 Dec 2025 01:12:17 GMT  
		Size: 599.7 KB (599661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:907c7a97f80a34fa39fdf8350ceb2fdd22e3d25ce9753ad7f48880c84478bb74`  
		Last Modified: Thu, 18 Dec 2025 01:12:17 GMT  
		Size: 43.1 KB (43112 bytes)  
		MIME: application/vnd.in-toto+json
