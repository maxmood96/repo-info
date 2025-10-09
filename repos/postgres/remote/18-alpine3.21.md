## `postgres:18-alpine3.21`

```console
$ docker pull postgres@sha256:c4238e5504e3c7d36f49dc918b12685d709a7e46549cd44a5b1e1f036f52ba57
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

### `postgres:18-alpine3.21` - linux; amd64

```console
$ docker pull postgres@sha256:5ec963b6a07c4f43e4a6ec7a62e6db66a255473a975736b15eb4e7448c2921e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113772995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b04c0ab25bfdba34035523dd02c9a0c88e27ba622aff2a44bc3bc495feb65d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=18
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=18.0
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=0d5b903b1e5fe361bca7aa9507519933773eb34266b1357c4e7780fdee6d6078
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7102769101cc56f144ddedc58d388f88e7f843b1119d170eb216e86cff0d9691`  
		Last Modified: Wed, 01 Oct 2025 00:30:52 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16e1b4e8fe48664799d31807a094b36b24d6f0c8671d69db69edcc40fad05a4`  
		Last Modified: Wed, 01 Oct 2025 00:30:53 GMT  
		Size: 915.4 KB (915358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3caf5cdf6f22401896fa459fb449f98b8ef667f5801f04c7fae8c879238747f0`  
		Last Modified: Wed, 01 Oct 2025 00:30:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36ee63dab2647775711f6a2434784602126e9e2b5bb0006802703dda6b3b2d3`  
		Last Modified: Wed, 01 Oct 2025 00:31:02 GMT  
		Size: 109.2 MB (109193778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4df7432d550f6fdef450dcabb047ab0c234d42b012811a9b2bc3767224fcb3`  
		Last Modified: Wed, 01 Oct 2025 00:30:57 GMT  
		Size: 18.8 KB (18775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2d99a4643b7bb54bf62d4f1e3f10741190c4df304e4bb24f42b5e1e9b12752`  
		Last Modified: Wed, 01 Oct 2025 00:30:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b39ceccb1abae4ea9fbc059e85857a44e598c962975239a4590fc2b31de57fc`  
		Last Modified: Wed, 01 Oct 2025 00:30:58 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587b453c690c9ebebdbfadc4ce33a6a9cd722ae93faf3f3e2f1638ac10e35506`  
		Last Modified: Wed, 01 Oct 2025 00:30:59 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b1d86de173546b5be6af1d895e74750aa4ec7ec47eb24ebb42426053c27fee`  
		Last Modified: Wed, 01 Oct 2025 00:31:02 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:e41df4ab3bf18c8b39243cff58a65a4bf3b54fa48d3cbd8df9642fd8202f010b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.9 KB (642854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3387384933a936336edc5f613630d03650606db80649725591f5ec4ad65b6d1e`

```dockerfile
```

-	Layers:
	-	`sha256:0dd4dd68470380e7638058d508ae1903f44cef8cd523610bd706e26687b7c205`  
		Last Modified: Wed, 01 Oct 2025 14:16:11 GMT  
		Size: 600.6 KB (600621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b63fc5302f801d37ecb90b9d837d7ec171b754dff04337eae0a48e9994595bc9`  
		Last Modified: Wed, 01 Oct 2025 14:16:12 GMT  
		Size: 42.2 KB (42233 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.21` - linux; arm variant v6

```console
$ docker pull postgres@sha256:522e8700787eea57c93aee1ad55fbd010e2bebf48da3808b8056357e71a2757e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91074260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84865c90e611b739301d0aff074c6a35a5a413c42038453ea1529b84f6bf61b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 30 Sep 2025 18:58:13 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=18
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=18.0
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=0d5b903b1e5fe361bca7aa9507519933773eb34266b1357c4e7780fdee6d6078
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f432460fed417a847f366711fd6a1511b2886effd39191b05aaf5ef6590f0d87`  
		Last Modified: Wed, 08 Oct 2025 22:04:03 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872e21f054224121d06fc6fe3f85c9a32f278d296a742f4724995a17b7e7604a`  
		Last Modified: Wed, 08 Oct 2025 22:04:03 GMT  
		Size: 886.1 KB (886097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c333154ed241d922433d4c11e95716b66b6867c29d3659667e5519c79ace292`  
		Last Modified: Wed, 08 Oct 2025 22:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c526d400868657875ba51fecbadb932713928d4731b20f08af9f765317136dcf`  
		Last Modified: Wed, 08 Oct 2025 22:04:10 GMT  
		Size: 86.8 MB (86796413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c49817f852a95efa49f04e8c1094f25c8a1c2856249c054fc7a4725e75bce6c`  
		Last Modified: Wed, 08 Oct 2025 22:04:03 GMT  
		Size: 18.8 KB (18775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c093ae684959648bf6c55cd789e886a882a7be66bb67d8fb291c10368705712`  
		Last Modified: Wed, 08 Oct 2025 22:04:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c69b574d7643bcf0effcc118cd2b164430929da1abf2a9bd99306c5ace156d`  
		Last Modified: Wed, 08 Oct 2025 22:04:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93014ccb8ec6c1da02e4d0eeacd120889104e076564bdddf657d7e9f7f95f362`  
		Last Modified: Wed, 08 Oct 2025 22:04:03 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579cda163b4079ce90b9dce92ac2ce5bc3fca9dc894a35e7fc1e325428552454`  
		Last Modified: Wed, 08 Oct 2025 22:04:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:c5819b34fc53f07b52828b942ec5c615765391b65a55d4512fc3fb8e71cbfa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 KB (42175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2bff477e07343509e288a929225e5b84d5d9cd46023a095344118e5302ceeb`

```dockerfile
```

-	Layers:
	-	`sha256:3f359a2bece998c021bfd55d9df5f441714ac04bbb58164de2aaec079299a7aa`  
		Last Modified: Wed, 08 Oct 2025 23:12:39 GMT  
		Size: 42.2 KB (42175 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.21` - linux; arm variant v7

```console
$ docker pull postgres@sha256:023682418b93bb3a62e87895fd9350ba080c8a94d4679664cc26313e43911beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86229781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87276906c4c9efcab6d3aabf49b2341bf155517d2fddb6387f09d29f068cd874`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 30 Sep 2025 18:58:13 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=18
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=18.0
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=0d5b903b1e5fe361bca7aa9507519933773eb34266b1357c4e7780fdee6d6078
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a0526f545ceb52e7c4539b0efe1414f2ef23f4faddfa238d59bb585faf65a6`  
		Last Modified: Wed, 08 Oct 2025 22:05:32 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aced2f51bc49ad5c9d4bbf3e969d4cb16c43813072b7e7e62463ecd17ef90989`  
		Last Modified: Wed, 08 Oct 2025 22:05:32 GMT  
		Size: 886.1 KB (886099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22627d9305c537eb8b351c790dbd46d18349e49bb766e0b0b131bb92e66bf88e`  
		Last Modified: Wed, 08 Oct 2025 22:05:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23034d3667b8fbf36fd943b7609fbd673b373e4bd47b968f33ebd595af698d25`  
		Last Modified: Wed, 08 Oct 2025 22:05:37 GMT  
		Size: 82.2 MB (82218789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a37035f4a63feccea71287dfd453f3a40ec715974277a7bf73f3483390cb06`  
		Last Modified: Wed, 08 Oct 2025 22:05:32 GMT  
		Size: 18.8 KB (18775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1e1e9d4f7741b029424844517d215f67fd5257c64319468f5682cc6875f80b`  
		Last Modified: Wed, 08 Oct 2025 22:05:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30e3e7f0e7d8d76608a5035e8ba79c842dad9393c730d9fd43d9b8954bc37b0`  
		Last Modified: Wed, 08 Oct 2025 22:05:32 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8632236c386b6724e2cb48c9d595ab0506886f50c32c3b726c86a986ce3d594`  
		Last Modified: Wed, 08 Oct 2025 22:05:32 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae31acccddc9dbb5f907371e22ace4e9979fccaccfcbc4244813fb62f74f1c5e`  
		Last Modified: Wed, 08 Oct 2025 22:05:32 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:070ae7ddd6778dcc64c25ea9f56cbb8f45617695a0f73b157b09bf8848181e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.0 KB (643039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a1089b611ec7c479fb6bf0dae91742547e345bd61086b2f7cd9210a3499dfd4`

```dockerfile
```

-	Layers:
	-	`sha256:f3718d363aa112218c0feb942847a6bac4d9bb7cb8f539c8987b3ab5517bfc18`  
		Last Modified: Wed, 08 Oct 2025 23:12:42 GMT  
		Size: 600.6 KB (600649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1876b58987e5d73f06dcd193cf6defd5042ca621ddf3c8eaad7237544232028b`  
		Last Modified: Wed, 08 Oct 2025 23:12:43 GMT  
		Size: 42.4 KB (42390 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:d50208add13ae53fa202bbc591082ca53bbefbb7a205202043616a1f481f1a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107389171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe13ef53fe61d1cbde941ebf18ecfb837fc081428e9cfa19dee50da6072164b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 30 Sep 2025 18:58:13 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=18
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=18.0
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=0d5b903b1e5fe361bca7aa9507519933773eb34266b1357c4e7780fdee6d6078
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb109cb213e6638b47f09a2ea8fd3e878ec3a2880d2b3c451738d359e776401b`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1177b333d5b1918e0e5d7b6316c7d43bcf8a06264771c28a93337e4583934560`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 873.5 KB (873452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ddaa50f560bb23b9cb141393c63de0bfcf5ffb6b6242dbb3015c39cfbca4d7`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6923cfd0e5dd3a10499f92b2508a81d1b5f7430b4eb1bedce95ccadc621beed2`  
		Last Modified: Wed, 08 Oct 2025 21:42:20 GMT  
		Size: 102.5 MB (102497085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fe69f60f95ffad1af433535034034844d34ac8c8b94505ab9ec4b8c24b1510`  
		Last Modified: Wed, 08 Oct 2025 21:42:08 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd8129134261242166749b433def76404e6410320d2409b22de501daaa38f4a`  
		Last Modified: Wed, 08 Oct 2025 21:42:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e702bab42da5edfa52537397c8b4db2011bb76b1955b6c462628bdba57d9b2`  
		Last Modified: Wed, 08 Oct 2025 21:42:05 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d00b511810254113bcfaebedd656cf444f0289e4243ba89d1aea357a5c0530`  
		Last Modified: Wed, 08 Oct 2025 21:42:05 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d238ee82a720b56a4d59119eb6a24ce07db6af522255688d54517cb645cc3711`  
		Last Modified: Wed, 08 Oct 2025 21:42:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:2c6b13a577398158cfecc9fdbdf49423e151335771e4c787a45478cda9eaf8c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.1 KB (643095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949eb3a816bba220d8c421864c6240bdd8daf3f6e17f054f0164270969c29820`

```dockerfile
```

-	Layers:
	-	`sha256:cb3edd3ca43fbcdf7c799d239a90104af21ba2c17f732635088cd53f842ec2c3`  
		Last Modified: Wed, 08 Oct 2025 23:12:46 GMT  
		Size: 600.7 KB (600665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d2aec74051f7547d8a7d19f46f0e7ec4e9993727530a360ef171fcbe560d369`  
		Last Modified: Wed, 08 Oct 2025 23:12:47 GMT  
		Size: 42.4 KB (42430 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.21` - linux; 386

```console
$ docker pull postgres@sha256:a1b970f2f49e1996fff6943783fb5c435cd09601e196e366dcbe2443ddfb644f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117752892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:693180d4087854abab1822d8d4db18a645ffc7a98cf26992b16d35b5fd388def`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 30 Sep 2025 18:58:13 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=18
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=18.0
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=0d5b903b1e5fe361bca7aa9507519933773eb34266b1357c4e7780fdee6d6078
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8835e38c96a7ded4515bf29379fd5d24d04b9993046322a5d3b65f6c81b393ac`  
		Last Modified: Wed, 08 Oct 2025 21:39:07 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee440c2f9a4c03307dec85189bedc0c64c425f4bc44cf3d72fef11caa2d6a6f`  
		Last Modified: Wed, 08 Oct 2025 21:39:07 GMT  
		Size: 890.6 KB (890601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5392b17b9fb19c18070fdf58da3c2957e9e365d7d88290ca9dd0c13032a53435`  
		Last Modified: Wed, 08 Oct 2025 21:39:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a532c1c12af086cf839b1cd550fbe87b18a0c97c406610a69a5fb55e3b250d6`  
		Last Modified: Wed, 08 Oct 2025 21:39:17 GMT  
		Size: 113.4 MB (113371298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cf8a48d261afed97e707bc4865df60faa8e88050a105388b0d0e4714f47b1c`  
		Last Modified: Wed, 08 Oct 2025 21:39:07 GMT  
		Size: 18.8 KB (18779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f615d3696f766a2b216202eec46f24dce7bdb37227ba123feeadee64a8a29ea1`  
		Last Modified: Wed, 08 Oct 2025 21:39:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc2e0bf15a576ca9d0613d3aa1bb82f1fedebfff8620806a813067218846447`  
		Last Modified: Wed, 08 Oct 2025 21:39:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762b89c659490d6f7771abc8ca198e168ea6de58a569db4ed1e793dff6a2b75c`  
		Last Modified: Wed, 08 Oct 2025 21:39:07 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1f9440a57dd4bd1caebe66c2e9179931c5e6b6611cc8643db5d17d5cac91f9`  
		Last Modified: Wed, 08 Oct 2025 21:39:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:a317e9ac0d576f9b84c316896bd4a4bb89cf170595d50897293c1328b979c12c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.8 KB (642793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948bdd906b06ea7066e626e6576ab660739479bc72e49f467ca0f22dceecfd52`

```dockerfile
```

-	Layers:
	-	`sha256:2197f1047c0087519f3b084279f084bd2cbd96ff8898f4bbb00b351d4a1831d0`  
		Last Modified: Wed, 08 Oct 2025 23:12:50 GMT  
		Size: 600.6 KB (600601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f401049d2bab459121c59e7a8ceba7a2b18144ec91cc0feab04d5e4a7d9a5fb`  
		Last Modified: Wed, 08 Oct 2025 23:12:51 GMT  
		Size: 42.2 KB (42192 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.21` - linux; ppc64le

```console
$ docker pull postgres@sha256:e51a909bfa05d375c8fc24b7956d08e233a494b0159142c845cfdf32e4bd159b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97551603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c817e34111a8cbc3be712c57012fab6777f4c0f3b4c72b44850e0dfc0111a888`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=18
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=18.0
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=0d5b903b1e5fe361bca7aa9507519933773eb34266b1357c4e7780fdee6d6078
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747bf6778b8e7ed31d4743686f1f50485c5c074620417743c59a087cdb5f9186`  
		Last Modified: Wed, 01 Oct 2025 08:36:58 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ded0eec492104ecd2eae20f50bf37ad15ee8c2428edc86b79a41ad80e9addb`  
		Last Modified: Wed, 01 Oct 2025 08:36:58 GMT  
		Size: 873.8 KB (873763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945b6b6d1d53681606965ab264b776b8bb57d1abfef335c32cdd28e6de23f19f`  
		Last Modified: Wed, 01 Oct 2025 08:36:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919c98cb0844ca0ebae1951848e025d694b1ddc4b04ef192ad4385bc925668af`  
		Last Modified: Wed, 01 Oct 2025 08:37:12 GMT  
		Size: 93.1 MB (93082418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3179c8adbe21aa03ef0d885ab2e66c8b97c4af660cc2db17518083b1069b81`  
		Last Modified: Wed, 01 Oct 2025 08:36:58 GMT  
		Size: 18.8 KB (18782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9202a97115f0499f2eb4387a2ac3cc224ebc412fc3a89d905f5c8689025747a`  
		Last Modified: Wed, 01 Oct 2025 08:36:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c53fcaf01fb01a6530bcd3a7f1a1510c4f0198c894a4a706d9d77425532ff6`  
		Last Modified: Wed, 01 Oct 2025 08:37:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f787091719fd20ab9cbe038bd0cddae568bb794c2b1d50e1adf12f664fa3cc2`  
		Last Modified: Wed, 01 Oct 2025 08:37:02 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5f9e8231bdde6a193be80ba52d96174b830f327d668d596fb23207270929ae`  
		Last Modified: Wed, 01 Oct 2025 08:37:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:82de48775285dfadefd8af9f71dcc3d787f7abd90b91dc3bba40f9cf5c1bc4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.3 KB (639315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7366fb299efd77aaa2768f6a65575ec04bd306a2ff10957f2f5cd2397994c01`

```dockerfile
```

-	Layers:
	-	`sha256:bf996721f78d90c1447391d679448f100637c77a5eb1b7c655a0c93140615aa4`  
		Last Modified: Wed, 01 Oct 2025 20:17:43 GMT  
		Size: 597.0 KB (597036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8628b5916a008e3e521ee53c403c3730b488893addb16d7b849dc8ec2d58a379`  
		Last Modified: Wed, 01 Oct 2025 20:17:44 GMT  
		Size: 42.3 KB (42279 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.21` - linux; riscv64

```console
$ docker pull postgres@sha256:e69995491beb0d0cc8d31ab18b2e0524151a0916cd51ba5f2c189137a6ff46d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111676502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6d6bc3fdea83ebd3f7525ba1e624f47a482773d59e190b6fa5c061dfc88a6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=18
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=18.0
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=0d5b903b1e5fe361bca7aa9507519933773eb34266b1357c4e7780fdee6d6078
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f442f14b9fc184be7b5b23f9b5362306d14b41b75f0fc847fcc5851ab3402e5`  
		Last Modified: Wed, 24 Sep 2025 00:47:22 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a806fe08f5cb13a300574c46c89d7d784c57ea301fece231af5a28695589eac`  
		Last Modified: Wed, 24 Sep 2025 00:47:23 GMT  
		Size: 860.8 KB (860848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb7abe1548e88b5e00e91420dec591721dc5e28906366569ea3c754484cf079`  
		Last Modified: Wed, 24 Sep 2025 00:47:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8a4e462be65728d02ee01b34b1e7e7040c547ab0a6b352ea259c7686aeee98`  
		Last Modified: Thu, 02 Oct 2025 14:59:31 GMT  
		Size: 107.4 MB (107440260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d310ff5e74a85f589803f7a6e4d7695bb792aa0e527a880608e2fa0c95382e5`  
		Last Modified: Thu, 02 Oct 2025 14:59:15 GMT  
		Size: 18.8 KB (18785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721792cc534bb5602acfb425328e347c05b604502e36e41dcc14372aeba6d1bd`  
		Last Modified: Thu, 02 Oct 2025 14:59:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a7c421d052a95947368a1cac18351f5fcafb8da977ab9ff097450fcebe1040`  
		Last Modified: Thu, 02 Oct 2025 14:59:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6034951bf42e2394a18883a0d22cd6754af9d48052ffa76087072ba31efc4`  
		Last Modified: Thu, 02 Oct 2025 14:59:16 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deabe33b212ad4764d6f76985cd2ea65d1cbd2928288a614d18c61da4031994`  
		Last Modified: Thu, 02 Oct 2025 14:59:16 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:c44e0eda6ce36f75e743d4fa26d3d2120f94cd4ac92a68558a6b01ca6374c165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.0 KB (640977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a220ba82e3301e944d816409b449c287c12dcd65189f23298d8cb45b86f7c94`

```dockerfile
```

-	Layers:
	-	`sha256:fcba92afdd4889e8cd757e1e1187a9c59281bcdb0ba4ef10559483313579668b`  
		Last Modified: Thu, 02 Oct 2025 17:09:13 GMT  
		Size: 598.7 KB (598694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d7c178b4803221c8766ffbfe4bc4c143738a9df156bc8e70eb0d2bfe139e78e`  
		Last Modified: Thu, 02 Oct 2025 17:09:14 GMT  
		Size: 42.3 KB (42283 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.21` - linux; s390x

```console
$ docker pull postgres@sha256:cd9bfedff9fc4d57e0d30d315a577fec4b5bd2c2326f183af256987b48fb3d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122214319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7351fa7b739f8516ad22c6dc608b3188651ae3a41193d9f8f892812c1caf9ef8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV LANG=en_US.utf8
# Tue, 30 Sep 2025 18:58:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_MAJOR=18
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_VERSION=18.0
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PG_SHA256=0d5b903b1e5fe361bca7aa9507519933773eb34266b1357c4e7780fdee6d6078
# Tue, 30 Sep 2025 18:58:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
VOLUME [/var/lib/postgresql]
# Tue, 30 Sep 2025 18:58:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Sep 2025 18:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 18:58:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Sep 2025 18:58:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Sep 2025 18:58:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3a0b3e42a00821c504172afe5ad33497b04821fb945d8f1762c22b804de062`  
		Last Modified: Tue, 23 Sep 2025 22:00:10 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfde9cde752b53d44f7ef28a4eaabe5d98c6054f6df4adb3d525fe6d7846494`  
		Last Modified: Wed, 01 Oct 2025 04:51:03 GMT  
		Size: 891.2 KB (891242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84ebe1c43984ac63d7ccb1f231905711b31a9170693143fcb9b288eb62b2ab6`  
		Last Modified: Wed, 01 Oct 2025 04:51:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8de73c2ac4505b784aac79cf6312e065b89ec0925f99c8765c882259363c14`  
		Last Modified: Wed, 01 Oct 2025 04:51:14 GMT  
		Size: 117.8 MB (117834695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f03b19cf64140b8bc2b884eecdd9d91c3df22c31a5f7cebb995577686ad29e`  
		Last Modified: Wed, 01 Oct 2025 04:51:03 GMT  
		Size: 18.8 KB (18773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5036ec4a5bf39e206640ef4e0cf06c871b519be0fab2cb03180961c4475d9c41`  
		Last Modified: Wed, 01 Oct 2025 04:51:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bdcd05a074437027f39bdbed76a7227d0a75d34d170759c684ced4a3f832b7`  
		Last Modified: Wed, 01 Oct 2025 04:51:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121e9e02bc551788d7edefc91b0e810d43d4728f0cac6aeebf2d2fef897389a7`  
		Last Modified: Wed, 01 Oct 2025 04:51:03 GMT  
		Size: 5.9 KB (5924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f7838e3478d3654cadd75622ef66b7922b09e1ebd90715575ed550b4011a27`  
		Last Modified: Wed, 01 Oct 2025 04:51:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:f5520eb6681e91be750178f1af72b78e1dabcf1963f8e66acce47b46e64c4b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.9 KB (640903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae50d74e6ffbf7c8c37d059a74925b43479483c1237be99d700fead65c4a1e7e`

```dockerfile
```

-	Layers:
	-	`sha256:3d82e88b3eb8e9ff58b3fd9b324bb8d5ef6ac63e8f052440e2c1c2efd06e9bf1`  
		Last Modified: Wed, 01 Oct 2025 20:17:50 GMT  
		Size: 598.7 KB (598670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3923aabb557052386a50ccb480e1e7e0f332fb900fb7eb3647968d4fa2fafdc`  
		Last Modified: Wed, 01 Oct 2025 20:17:51 GMT  
		Size: 42.2 KB (42233 bytes)  
		MIME: application/vnd.in-toto+json
