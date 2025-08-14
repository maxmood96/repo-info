## `postgres:15-alpine3.22`

```console
$ docker pull postgres@sha256:2971a22cacaa39b2107e328fb31da85311aa02c91ebbebb39b3987d58bb019dd
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

### `postgres:15-alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:dbedb0e3d02d268e77b6966910404b748bd390a9dbcb91216303349bbc4dc1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.9 MB (108855784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06686173a6ebc27c0f4687565ae0fe73342ea23d1e3813264ded5f5d2b29fe28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Thu, 14 Aug 2025 16:40:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a7421693bd58461f5d165da30c561e55dd2ce1f2f03cb8d79c32db60af07cb`  
		Last Modified: Thu, 14 Aug 2025 18:24:01 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a939567803e1b9c654a71ae505ed9f9815ccc93bc0bcab0cdd179a81cd99d7`  
		Last Modified: Thu, 14 Aug 2025 18:24:01 GMT  
		Size: 1.1 MB (1115586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a612d38c9b48b45bedb526c539f36d4a14f98b6239ff45e9c8e124e33d318f3a`  
		Last Modified: Thu, 14 Aug 2025 18:24:02 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901a9540064af4d0ef3a4c524cf3bd73b50e7774df6b43228da0ab319458cb35`  
		Last Modified: Thu, 14 Aug 2025 18:20:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c13c55b4b82da0aa24053d932b0e4c06c789c283921f5872e85fe1e5f540cbc`  
		Last Modified: Thu, 14 Aug 2025 20:11:11 GMT  
		Size: 103.9 MB (103923389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f940631c13ffa8c4148c1d546121e852c432644b39c12e29d145fd813ef6d56`  
		Last Modified: Thu, 14 Aug 2025 18:24:02 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15854d6fd91d44215f0b1f2009926be64ee77c7b1b14ca8c722eaaf778c6ece`  
		Last Modified: Thu, 14 Aug 2025 18:24:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685be96195b78ff0bbf6dfdd8dcf9acb224aee415d323b1673002c825f055e99`  
		Last Modified: Thu, 14 Aug 2025 18:24:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce414b3fa6741850b575d7e8640d0a94e06c715b45026d103b4589144cb832b2`  
		Last Modified: Thu, 14 Aug 2025 18:24:02 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afcd9ec0fd973fb5b460a79ff4265372732624a3b813f4ea69925c71d6bfc9d`  
		Last Modified: Thu, 14 Aug 2025 18:24:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:0d37dde9076f44722888d36f6f83a1969bb31459f6411742299c5cbb5facb2a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.3 KB (641315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfef01efc908ade47e661d12ae76c965b55f4eee9a1dc23b238b9595276e230`

```dockerfile
```

-	Layers:
	-	`sha256:593d809f8f64f6ee04de8a485940f320f9f2d27b78d8f0dd8bd6cd1522ec5254`  
		Last Modified: Thu, 14 Aug 2025 20:11:12 GMT  
		Size: 596.9 KB (596941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9429ad005e88c0269c87ea807d6dbdeec64ac35594c6c53e678dd821d0a28722`  
		Last Modified: Thu, 14 Aug 2025 20:11:13 GMT  
		Size: 44.4 KB (44374 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:8ddacc8b372b4394e14422221c3ec337ad553d75c6d5988be45b57df4ed66705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88467518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4828c9fca04c52759a426d009d93e8f857e0234a8a4230a953410ebfa99611ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Thu, 14 Aug 2025 16:40:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079a1c87b1e4afd06564bb4788685a8121d0bc8ee1c65f7d29bae031097a898c`  
		Last Modified: Tue, 15 Jul 2025 21:59:03 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e018b614d5cbf1a0d8a1b23f428d5cbbbe192798ac0751d81172993ca1dbc93`  
		Last Modified: Tue, 15 Jul 2025 21:59:05 GMT  
		Size: 1.1 MB (1083508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7112f2e184ceefef9eeff37dd72d2f7909f3a223202968b7606e35232a4f6866`  
		Last Modified: Tue, 15 Jul 2025 22:16:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a57156ff7ae7b2ba746fdc40a1ad960d3dfd641362dd61bc3ad15b940144230`  
		Last Modified: Tue, 15 Jul 2025 22:16:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e112a6002f97f4852bef7f74274c12f3aa1801da16a8c86c60b634c07e0004`  
		Last Modified: Thu, 14 Aug 2025 18:45:37 GMT  
		Size: 83.9 MB (83865982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbbd013787c8264ba9008818700ad39366fce0b0896029af4f94a67982289d7`  
		Last Modified: Thu, 14 Aug 2025 18:45:31 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d099f4a5cda740f8bbe28bddfdeae3fbb5193058cc8335422a363dec068166`  
		Last Modified: Thu, 14 Aug 2025 18:45:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7c112c3537d6d832d50d7c28ccc1b25ca9c0ddfe05da6d7d7dafd73a56642f`  
		Last Modified: Thu, 14 Aug 2025 18:45:31 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7741fda6e53f9fd2d45df0b6fb6f26c8b7218972c1c70bf4954d87d7f0c0e9`  
		Last Modified: Thu, 14 Aug 2025 18:45:31 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3723bf23652f01085e768811c1f12a588396255771a1e97dccc5deec5539bfbf`  
		Last Modified: Thu, 14 Aug 2025 18:45:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:6724289dbd1463e62dee0b979b9169dd7b0f212003af57272efeff7d4e0b4c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 KB (44333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3156325723ed065240e205f6c57bf4bb2168eb03bc523d97e4aa37ba91c52b`

```dockerfile
```

-	Layers:
	-	`sha256:d99556d6acb7c590da259a538fec5bf0deba8b55dd67e4f4b6fb3a59fc3f8a9f`  
		Last Modified: Thu, 14 Aug 2025 20:11:16 GMT  
		Size: 44.3 KB (44333 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:9986ff5c03dd7b76206ecf77994ca95b13481c3edf4398726c86cf86c9b68e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83757094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88dddeb0614419c1ecb7894e7742e724e74c59f2fd393e9d9ff406267942d71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Thu, 14 Aug 2025 16:40:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d311585bee083aa9525f093872b6272f30fd05678140622cf8b253423af3dd`  
		Last Modified: Thu, 14 Aug 2025 18:50:36 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36a7751694a53e9a57d5356c38e15bbc8420fe128dc24f6b1156e5d65657148`  
		Last Modified: Thu, 14 Aug 2025 18:50:36 GMT  
		Size: 1.1 MB (1083514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbeb9513aa078b0eb8ce4bf6d95a7b7787beb9460a2af8d19a69c827e22729b`  
		Last Modified: Thu, 14 Aug 2025 20:10:32 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b458e6c32b35c52476942d750d16263a199db15b9a6e0c8c603fca6a5f8a2f1e`  
		Last Modified: Thu, 14 Aug 2025 20:10:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc66c5e581884b713e50d138ae0b2a05acbf9fe59949441aa9b43261de3fbe07`  
		Last Modified: Thu, 14 Aug 2025 20:32:55 GMT  
		Size: 79.4 MB (79437417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8d40f20fd09f836c502440e758f2eba8ddb2e48fe0e59158cc54f94ae3c6dd`  
		Last Modified: Thu, 14 Aug 2025 20:32:32 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29ddb85975299aa89fd68a8502433584d6e2da052b32c97b04acb3fbf445fa7`  
		Last Modified: Thu, 14 Aug 2025 20:32:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c7d9b827c74155e51ef78cb6bd9e0d5fb17c75ffad5650b75f51bc048ee9ce`  
		Last Modified: Thu, 14 Aug 2025 20:32:32 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187026e01ff15c3effa4f02826cdeeee3bb4e24c89efcc04fdce416804c610a6`  
		Last Modified: Thu, 14 Aug 2025 20:32:32 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9821b2a77ddfa3bd48555cd1d025055edaeaaf35ef253afd727718beb4ed0da`  
		Last Modified: Thu, 14 Aug 2025 20:32:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:b889f0a660f60433ae9a9bbffbb24fc41d096d5ced6c2e9a8318625d17659680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.5 KB (641524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c13f0ac123fa06269028a70a21a926e2f2dc467399f97195a90b7b78137158e`

```dockerfile
```

-	Layers:
	-	`sha256:61a8ef23c63b58fa5bd6726a20c898cb70af5c95196f2946d96978b0a86290f3`  
		Last Modified: Thu, 14 Aug 2025 23:10:23 GMT  
		Size: 597.0 KB (596977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b808e62a56778a09778f0fdaa13ccc31da66b9af18c5226ea5ab074b70d57df5`  
		Last Modified: Thu, 14 Aug 2025 23:10:24 GMT  
		Size: 44.5 KB (44547 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:fab2451398ad2d9dd2e22a05a1a05f65bd1c34e4f3d4c9d36e94a4fcb4359e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104777293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c7b113e79486df0dc58e9a384efc963b85d2a108d09572b4c2772606c8a923`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Thu, 14 Aug 2025 16:40:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5c482840cf82de196008abc359484735770b13c9282408f1dca4d75164f7d5`  
		Last Modified: Thu, 14 Aug 2025 18:54:31 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e157a09d862e13d8d0e716ab97e9d5a2c94438123a639c16e3eab984125883e`  
		Last Modified: Thu, 14 Aug 2025 18:54:32 GMT  
		Size: 1.0 MB (1042499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beeac069caed963f46280d25489c8441ffe149df80d1667eb2108c8069089456`  
		Last Modified: Thu, 14 Aug 2025 19:09:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fac8997d1dffe2a81af36fccbdaf990b3b0a3dd0146bb736836b02cfc6164dd`  
		Last Modified: Thu, 14 Aug 2025 19:09:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af53d363b675c37f171bf3d0cf93175b27559c2fdea55f53926626ca060ba61`  
		Last Modified: Thu, 14 Aug 2025 19:17:39 GMT  
		Size: 99.6 MB (99586915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690be4e8a00522667ad5867dad00b863f07cec582154cd49f29f39cdd3542944`  
		Last Modified: Thu, 14 Aug 2025 19:17:34 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43106089ad38b9c4fbffad9078a3a9736eb7ed0560ca2a7ce1b66980b16e5cf3`  
		Last Modified: Thu, 14 Aug 2025 19:17:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb18cae851f6d024a45e944c18de2aa7bc7312468bfe19fdba965587c21a564`  
		Last Modified: Thu, 14 Aug 2025 19:17:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afe90f8c9c688c7c6e7ccae67db21c036bdf73428bda45e38d012acfee159a3`  
		Last Modified: Thu, 14 Aug 2025 19:17:35 GMT  
		Size: 5.9 KB (5932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f7812c4728e38f13ad569c9c5152ec49d9612615e222fce4645158c71b5fbf`  
		Last Modified: Thu, 14 Aug 2025 19:17:36 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:5196244acd051496fcfc073c4829af2030b4566b8f22c1f296d5b884674240d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 KB (641589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:864fcae8ad88dd54767dfca30023db1a2d1e88be11a4d608d298a39a4dc04140`

```dockerfile
```

-	Layers:
	-	`sha256:33fadf2bce17df10858689b14fb6843ebd648d38a8f2df43d23c19791987f85a`  
		Last Modified: Thu, 14 Aug 2025 20:11:22 GMT  
		Size: 597.0 KB (596997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea684da592636c70f4d64a88802e0f2c0eecb82f0b062a82cb7bb1a6a15d696`  
		Last Modified: Thu, 14 Aug 2025 20:11:23 GMT  
		Size: 44.6 KB (44592 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:617afb60eb3fe6f1b294f995a6727163b7f5c9284e603ca04be88249a028361d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115116305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:944aa5d2986eede6b95bbd765bf10aa48db13e4e8d20525b2aaa1a003530558a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Thu, 14 Aug 2025 16:40:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3877660aba23809bcd28ca20348884188ca6c4228179f8857ae040c772a3c826`  
		Last Modified: Thu, 14 Aug 2025 20:34:38 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbbc365d40b673829b7626d0efc36f616119ad29e5d3f27fbf4576c1e289659`  
		Last Modified: Thu, 14 Aug 2025 20:34:38 GMT  
		Size: 1.1 MB (1091509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab595751855ce7a902e734b447fb6b86a69232d669412f2b554f2d97e1457d4`  
		Last Modified: Thu, 14 Aug 2025 20:34:38 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c27868070f0aa5ed6dc4a94e747eca21524fd8dde7d09e03e755020754ad0a9`  
		Last Modified: Thu, 14 Aug 2025 18:20:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd08fd30fe7d67648f16633c8223f7607728559010b150fa5c0a8633a70b941`  
		Last Modified: Thu, 14 Aug 2025 20:34:53 GMT  
		Size: 110.4 MB (110392672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbe427626b8a2b157b28b4a11b14b5c808dacb1538e6bc10e3d419ea0005d65`  
		Last Modified: Thu, 14 Aug 2025 20:34:38 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e487e9bdb216f7f0a2f3c78e411d2178f331c9133014ee47ce51562fb2458605`  
		Last Modified: Thu, 14 Aug 2025 20:34:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87d6f160184e7aac73b5e9736a00f97c8204ef4c6961fcfaec9113d6417641f`  
		Last Modified: Thu, 14 Aug 2025 20:34:40 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3298f3cfcc8e69db1d1e6cd3002b7a763cbcc7abaa2c107695669a8e35fcf4ef`  
		Last Modified: Thu, 14 Aug 2025 20:34:38 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc437b724a923f0c306c9bbad933513e5ebc882041fcde262c8d12c8969d875b`  
		Last Modified: Thu, 14 Aug 2025 20:34:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:3a416c9977974dae99cce724f207ad2e6e45013d3b76b2558c0695cce74bbdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.2 KB (641242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fda4bf683f24272afe62cdb37200e48238eb11f2cddeb6656223684ff69372b`

```dockerfile
```

-	Layers:
	-	`sha256:42c263b438144912bde3b9e4d3ae827fb49cec68cfc893adb3b2d8066f846572`  
		Last Modified: Thu, 14 Aug 2025 20:11:27 GMT  
		Size: 596.9 KB (596916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd80c321921bb05285d875c4febf13b810d07c1d8add37eef2eeacedaf982bd9`  
		Last Modified: Thu, 14 Aug 2025 20:11:28 GMT  
		Size: 44.3 KB (44326 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:3e5806b36e23d488615412033861e6c041be1b71ce6b43b2033932de4412c2bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92566408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb07cbf210b8b8c9e4064ef641b498cf1ab48c3b9b838fd92f01fb700c6fd7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Thu, 14 Aug 2025 16:40:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5ee779caf31f6000861b5a827cc767777a7e523406271d594906edba47fb17`  
		Last Modified: Thu, 14 Aug 2025 19:04:33 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39e84474c9e8b921b5d1f181c420c8539aaff375b40eaaf2fb3eaa645a3f1c3`  
		Last Modified: Thu, 14 Aug 2025 19:04:34 GMT  
		Size: 1.0 MB (1032220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94ccd247fc85b417afdbafd53b06d2487171dda880c5aa0bd753a507fa6bf9`  
		Last Modified: Thu, 14 Aug 2025 19:28:31 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e2935a77d21eae07c28aac1c8fc1cacc4234ba4c89db92756482884273dd1a`  
		Last Modified: Thu, 14 Aug 2025 19:28:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c17d878bdcccdba600906925f69110c1721ec1c9a60a5eefc8b865016f10de`  
		Last Modified: Thu, 14 Aug 2025 19:39:57 GMT  
		Size: 87.8 MB (87789945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34294facb6d108d8ab4eeb7a3e36834645e2f844385cebb741f2154b10dda2bd`  
		Last Modified: Thu, 14 Aug 2025 19:39:53 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5846ee765d8777d53c298353ae0d3bc513df29bc1d008a9364ade5eb6a16e261`  
		Last Modified: Thu, 14 Aug 2025 19:39:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5073a393a256d17e7320bc57ff4163dec25132b2d14ff7ab3fd66fd220eb8b6`  
		Last Modified: Thu, 14 Aug 2025 19:39:53 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e91ffd28eb3fd120817feac9799dd9093d40aeef3f5ed5bac1138328cf6dd26`  
		Last Modified: Thu, 14 Aug 2025 19:39:52 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c28f17fb8200db61b5e59e3d7de05133d1310f47e77b8e8831f650ca4914cb`  
		Last Modified: Thu, 14 Aug 2025 19:39:54 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:348d197c3bdab02bda0a76077c0ecd08e8de1b4e5d95e2946e9be1cf94fdd6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 KB (637790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc2173fda89d3fc6ef17e9e763469b500e44e16253b5492ec7a520d0379079a`

```dockerfile
```

-	Layers:
	-	`sha256:4defb1c483e92201039488c1026c771ba3bc587a0a6b2d82697b0bc655c46127`  
		Last Modified: Thu, 14 Aug 2025 20:11:31 GMT  
		Size: 593.4 KB (593362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cd51c351910e09adaadbb7d3773fdf22e994fee9ad8dff836a02932c4289dee`  
		Last Modified: Thu, 14 Aug 2025 20:11:32 GMT  
		Size: 44.4 KB (44428 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:4836475c2882de6238a87ee664e423e9507df781d604a3d8d0ea2973257338d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108797106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f749a317d0fde1a8ec838ff111715222c3b394632889eabdb1ff149ec3a5385d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Jun 2025 18:27:47 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
CMD ["/bin/sh"]
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV LANG=en_US.utf8
# Fri, 06 Jun 2025 18:27:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_MAJOR=15
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_VERSION=15.13
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_SHA256=4f62e133d22ea08a0401b0840920e26698644d01a80c34341fb732dd0a90ca5d
# Fri, 06 Jun 2025 18:27:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Jun 2025 18:27:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Jun 2025 18:27:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Jun 2025 18:27:47 GMT
STOPSIGNAL SIGINT
# Fri, 06 Jun 2025 18:27:47 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Jun 2025 18:27:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e4bf5c01f5fd5d5c2b6c78d1d884c92b6fce072812c2b64d8f250b5d9d572a`  
		Last Modified: Thu, 17 Jul 2025 04:54:24 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac990c2f318af1f8860277d49db61df409ca94944240be61871dfc66778de791`  
		Last Modified: Thu, 17 Jul 2025 04:54:24 GMT  
		Size: 1.1 MB (1085426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca4a60e5e84fee836f7f541710455c96ec0d3e445541a966a1d9f2df588a229`  
		Last Modified: Thu, 17 Jul 2025 08:31:18 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4e3883d3c5cb446972332da51687503a675e33ff0025674c2345ee1e0b2c2c`  
		Last Modified: Thu, 17 Jul 2025 08:31:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e321121607ccf681c4cdad47f74bda51a47e7022893fd9a7d91be944482109c`  
		Last Modified: Thu, 17 Jul 2025 10:15:09 GMT  
		Size: 104.2 MB (104181748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbd58d94a6490165e41b2b3a40620f3cd6457baf2ffc59b2fb63708c569224e`  
		Last Modified: Thu, 17 Jul 2025 10:14:49 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1800614333fd5d1507cb500fc519e8496c167032c0871c3b986ed0838fb0045`  
		Last Modified: Thu, 17 Jul 2025 10:14:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbd082b3e97debd9adefd0cc83bae0a28383f7d974115878584926021f692f6`  
		Last Modified: Thu, 17 Jul 2025 10:14:49 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f4fa0e64a96ec0c7dda11c618f4c9466d56aab7dc9eebc3f3c27a08a176643`  
		Last Modified: Thu, 17 Jul 2025 10:14:49 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a470ca7346d8d2f9dca88104ac62012b1ea9ceac2995bef8eeedb0de68c77f2a`  
		Last Modified: Thu, 17 Jul 2025 10:14:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:03347287f165597e04f04dedc30a8a4f4d65b7d0f292915947ec6f42f613d91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.5 KB (639454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11eba53575a281499c596da74ba7e348bc03ecc0c6673744cfdfef16d766e859`

```dockerfile
```

-	Layers:
	-	`sha256:e7861c98872cec2404e77aac2e20f962ea2f8d5f9aaf68cd3d16bcb6804900b9`  
		Last Modified: Thu, 17 Jul 2025 11:08:09 GMT  
		Size: 595.0 KB (595020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92cb692f5ecb1f519d733eb6338d9b13cb51c698acd43b512deda0e252a4ede4`  
		Last Modified: Thu, 17 Jul 2025 11:08:09 GMT  
		Size: 44.4 KB (44434 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:104a4e8b9b9e690fa9d6e15371bd66203625984d9b53c941d4104e2333e01de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117544477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889bb22ea34fb264cd98261961b3d73444e829870e873cb957f503698c460140`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_SHA256=06dd75d305cd3870ee62b3932e661c624543eaf9ae2ba37cdec0a4f8edd051d2
# Thu, 14 Aug 2025 16:40:39 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d38346a6df0fbebdd4778252bbd39ccc90b12f4fad75fe53f1e3c72e66c3a5`  
		Last Modified: Thu, 14 Aug 2025 19:23:02 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0825e8e3a340fc788e6927d6d834d1119ad7c294a2a2b22dae232cf44b292106`  
		Last Modified: Thu, 14 Aug 2025 19:23:03 GMT  
		Size: 1.1 MB (1081138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c48dde862abb0bf8c1f4d6d3973dcd647cdc3c112341269fc042560074724b1`  
		Last Modified: Thu, 14 Aug 2025 21:07:27 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212811b83d554e8223a575869c18d4bdcde2acb8bef094cc619b59440c3584f2`  
		Last Modified: Thu, 14 Aug 2025 21:07:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b831026e5a0a893c7feba18ae185d805144e13e088b8ced48b3e421473d67461`  
		Last Modified: Thu, 14 Aug 2025 21:53:56 GMT  
		Size: 112.8 MB (112801242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbca906bf99003790afa76296892d278ac4fc2bbac62f63e8eff571b207012ba`  
		Last Modified: Thu, 14 Aug 2025 21:53:49 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2f930b4298a0ce3d75b6f8ece88fbdfa2a9e9c3dcfc09eea99b1284e40d1ab`  
		Last Modified: Thu, 14 Aug 2025 21:53:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7629f11e03da76dc1a5b4afb9e0a25a98bd43fc20ef3ebe96783f3b13274fb6`  
		Last Modified: Thu, 14 Aug 2025 21:53:49 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6f8120fde2db8ed3fdc94c3c6b8b1a09a8d0fdb85c8cf66542a86c2fed8641`  
		Last Modified: Thu, 14 Aug 2025 21:53:51 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d5703672dc440bd0d9d6fc9ffb82be93724376163c1e9f0581d90977d1d220`  
		Last Modified: Thu, 14 Aug 2025 21:53:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:d69046b53e8d918332be268ba61627e62d3bb44f5a93d7753cf3edc26d4f9c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.4 KB (639363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3bbcda6cb001c9f141d64241206179d3e31ed8bb149aef3228ae31178d4d9e`

```dockerfile
```

-	Layers:
	-	`sha256:c858439a0a9a540a3606601ffbea9c7a0a2aab49b305f8e1bdbb9923319db629`  
		Last Modified: Thu, 14 Aug 2025 23:10:36 GMT  
		Size: 595.0 KB (594990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5329747bc38ae3b181f28db0bdb55989c269f9f5d5bee61c700efc538111fd2`  
		Last Modified: Thu, 14 Aug 2025 23:10:37 GMT  
		Size: 44.4 KB (44373 bytes)  
		MIME: application/vnd.in-toto+json
