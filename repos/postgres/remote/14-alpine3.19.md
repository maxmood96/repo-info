## `postgres:14-alpine3.19`

```console
$ docker pull postgres@sha256:d00887817bd20f12702aa1140425f20be1b4de1002d2895d03b0f442227f0c5e
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:14-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:3871f7400945630b808f91f0865d3884666c20111ac15f6de0a1b5f6674039f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95308836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96ff84c68750e28af436f5030de0d247349ca8a32f8ed3f65c63f38b9a7e703`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=14
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=14.12
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efcfc090e3ef848e2873541711a0fa300c947c84c14999696f87369fa9281e4`  
		Last Modified: Mon, 22 Jul 2024 23:10:20 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293428b94bad2c510e22ae5f1169016c52703c419d40e91d8328b24f41815c72`  
		Last Modified: Mon, 22 Jul 2024 23:10:20 GMT  
		Size: 1.1 MB (1120293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df70769b4bdc023f4ca618d7b0ab2a4d8b8f3bc8f61f73d57cd0140cc1897195`  
		Last Modified: Mon, 22 Jul 2024 23:10:20 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7facfd523f74407a98959219ece9316b7a8162c5e4e6c4fa5612ecd5930cefbe`  
		Last Modified: Mon, 22 Jul 2024 23:10:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393ebdcbdfb1ed499813d284e2ba645c3c9fdb468c54e03f2942a43252172b0e`  
		Last Modified: Mon, 22 Jul 2024 23:10:24 GMT  
		Size: 90.8 MB (90752851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b851ec9b5ff99b1977180ee4d098a398106287004ac5a718975d20fe070caa54`  
		Last Modified: Mon, 22 Jul 2024 23:10:21 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfd30423365930ec97d03bd040ea32498cd2e774fa281f0dde5d04bb5ad01ab`  
		Last Modified: Mon, 22 Jul 2024 23:10:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2406e07649466e9f51300ff60e976add74fe53e2e83208a0fffc49c6a33894c0`  
		Last Modified: Mon, 22 Jul 2024 23:10:21 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fb01188abf915a33ea78c1a5a238661b27ff691d389766fe8f4c41dd2ba174`  
		Last Modified: Mon, 22 Jul 2024 23:10:22 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52da44bef2a58c7f6d37aadfdf717eeb89ab2d34d461cd290bb17e449e85792b`  
		Last Modified: Mon, 22 Jul 2024 23:10:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:e2539e2d670e47bcd86c325df8021db7ac581309e5a25a5fd6b7327664117fb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1013288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5158b7696b97b44752a533b044395d981eb415add31191b11936879b4938b16f`

```dockerfile
```

-	Layers:
	-	`sha256:a1470adc8241d100f56ab249b10a1554397c69f1998d1a3fba7eda698b261056`  
		Last Modified: Mon, 22 Jul 2024 23:10:20 GMT  
		Size: 968.7 KB (968685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38ddb989e4ff5c9bf2ec0a30ab06a2272fe64ca1771c13b2787fa34725bc0550`  
		Last Modified: Mon, 22 Jul 2024 23:10:20 GMT  
		Size: 44.6 KB (44603 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:134af8ff1449d7cbcb0b44efef9dd369fc33b5a7cb12c4f7557e37fb4f6f5c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94084125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c5cb2dc4d99a4e5d578193566ca31e545140ead1eda75779510e72064cc7ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:22 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 22 Jul 2024 21:49:22 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_SHA256=59aa3c4b495ab26a9ec69f3ad0a0228c51f0fe6facf3634dfad4d1197d613a56
# Thu, 08 Aug 2024 16:52:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92880c2baf59ed2b2161ddbd42912f3c667f88b880b2bf7c544e35241839cc4`  
		Last Modified: Thu, 08 Aug 2024 19:10:19 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61abd44f0f6a377f52eb7c5307b260122a9190bc60a8ebc1db65d929f490cb8`  
		Last Modified: Thu, 08 Aug 2024 19:10:20 GMT  
		Size: 1.1 MB (1086692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70361eae90d9585bb273a16d57620fe9982fb2233fae0aff2a0c20dc4102d53`  
		Last Modified: Thu, 08 Aug 2024 19:18:01 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfa82c1ccf85ec588942b557d525431c73d2d1c59629214d888e6d8341478f0`  
		Last Modified: Thu, 08 Aug 2024 19:18:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a689b3e2048e6a14c221b7c869cb0d16f5dd44883318f7466661307b11ee383`  
		Last Modified: Thu, 08 Aug 2024 19:32:45 GMT  
		Size: 89.8 MB (89805099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6e6ffced95323f30336555efdc67839c11bd6c7ed1aac69dd6fc8ce625363f`  
		Last Modified: Thu, 08 Aug 2024 19:32:42 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6422bbf189348fdcd08af6063384fe805f2ab9ceb822d0d309ecc2f58f8f6a5b`  
		Last Modified: Thu, 08 Aug 2024 19:32:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67d9cb47ed8795ede28b8e19bc2bebc05cc0d6ef2825f7d76c940c215105f42`  
		Last Modified: Thu, 08 Aug 2024 19:32:42 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b0a232eb698274c7410fcf9d55be662c40039cc7da55419a7ae0da08033f04`  
		Last Modified: Thu, 08 Aug 2024 19:32:43 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c41199217048f53dbf381d0107194850b839e945617775dba1ddc96d7fcc1d`  
		Last Modified: Thu, 08 Aug 2024 19:32:43 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:365302e7509b7ed995ee1cc94ee837ca3778f9e2c435c9abd13eb14f34b87995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 KB (44726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9878999ffc6537da897aca85c7e0ec17f4bf0cdc8aca0b7c4c6a6fdd416d4d`

```dockerfile
```

-	Layers:
	-	`sha256:4f82ccc3104c936651e532285f82719e34f4939d1b104e2f531e2582321a200b`  
		Last Modified: Thu, 08 Aug 2024 19:32:42 GMT  
		Size: 44.7 KB (44726 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:c4a236e87201849278945cabc9d2d8abc0ab233e2917f0c651b1ee7a32987dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88538010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d4ae6fcc79a75425f22798409e0c4bcbf39336f68a71de2c2f9ac066900112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=14
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=14.12
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e00ac6be43720c25c11d5f9f235cecbdb349b24568030205dbbc1527d0a2090`  
		Last Modified: Wed, 24 Jul 2024 03:47:29 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707689daf83e36f961b1d519207e7b06605e5f2b6c48bf51fb093eafc652af18`  
		Last Modified: Wed, 24 Jul 2024 03:47:29 GMT  
		Size: 1.1 MB (1086690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82c88f55a4ec532d4721d7d78cbd5bc8ccb32eec36ee04bae8f80546d6a2e9b`  
		Last Modified: Wed, 24 Jul 2024 04:23:57 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09cfc889019313c567344f8b705116887f023214f894333c8ab5d8049c3ce68`  
		Last Modified: Wed, 24 Jul 2024 04:23:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87be07fe684b5c17215c5d71f01a3ac8d46dadc5ea511dadbb10630d7bcbb876`  
		Last Modified: Wed, 24 Jul 2024 05:33:59 GMT  
		Size: 84.5 MB (84507570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734fe4c05bec10a92da8fd0862d6d43419b306eae63988b4e1915f26c7f22a0e`  
		Last Modified: Wed, 24 Jul 2024 05:33:56 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc32c00bf455af69eb80f49488f8dc49d043d2be710217330a6f94df9b6456`  
		Last Modified: Wed, 24 Jul 2024 05:33:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d49287bee7bb1e4efa9de8b1ec854c998bc0504944e26d2d5a281c5752b38e`  
		Last Modified: Wed, 24 Jul 2024 05:33:56 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bf96bb5eb068dcb54fc416ef7645b3da807eec3f5e1d05ca0ed76936a73716`  
		Last Modified: Wed, 24 Jul 2024 05:33:57 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d73ae80e8e81184cffed60a14a671d149d858d9b74c42bbc984d2be4d90536`  
		Last Modified: Wed, 24 Jul 2024 05:33:57 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:003f729cb81afbebc16f1ed60546cdcbf00da740f3fd7f94e1b6d660af66679e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1013466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6efdf3ff1f582fb172aecfd74bb6412e467ea22fac192bad8dab7ff22bed5e`

```dockerfile
```

-	Layers:
	-	`sha256:a627d25d455b4ae52297bfb29aa5d5e8408b4a0d4c264c65170c2bfae7ebfb1c`  
		Last Modified: Wed, 24 Jul 2024 05:33:56 GMT  
		Size: 968.7 KB (968705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ac8cdd7cf61c08d65bd96460879000619fc41927ed329009ad4a0ba6169ce30`  
		Last Modified: Wed, 24 Jul 2024 05:33:56 GMT  
		Size: 44.8 KB (44761 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:83871e885955d1e3fdbe1f778f6650edb0e21fbd6388b2f79a12971a9ab97a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94013011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faa4d9bd8785942b66116788a90830405af804f92fb7fae4a1380e45df51414`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=14
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=14.12
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7430eedfdfd07b02b245d76061e40a66e9d046eb109fb1dadf11e64547b096`  
		Last Modified: Wed, 24 Jul 2024 01:24:14 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991d9a143b679519e244cf5746ea3f0804454479728e9c8b07bdeb57b3b0e6f3`  
		Last Modified: Wed, 24 Jul 2024 01:24:15 GMT  
		Size: 1.0 MB (1049350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf93a3cb67aebfa1677daa91e5038804bd389b6299c087d01c6f76a9839cdce`  
		Last Modified: Wed, 24 Jul 2024 01:32:37 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446cd68e49014f9aff26d9af569920030ce9d9c3309f9f9bfa9dd0380254bea1`  
		Last Modified: Wed, 24 Jul 2024 01:32:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f45ed459d9c3e5639958eeddd166034e01dfdae98f169178a3aeca954a15727`  
		Last Modified: Wed, 24 Jul 2024 01:47:17 GMT  
		Size: 89.6 MB (89588545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9fe9ef0974c8dbce203313af80280a18badfe77ab603ea80e95ff561f6d155`  
		Last Modified: Wed, 24 Jul 2024 01:47:15 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b74ea6278cebb0d2bf6474ff749e4cba36fd889482e22a35b0f54f6cd9ce80`  
		Last Modified: Wed, 24 Jul 2024 01:47:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f1439bd1817f1d10b6a959bb66d5b37bf4da6cca027f97c46af5d870bab9da`  
		Last Modified: Wed, 24 Jul 2024 01:47:15 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f2e4952f507f5fac43b8a4f54db54494aebfd6ab70570ed77d57a3b0f68b8b`  
		Last Modified: Wed, 24 Jul 2024 01:47:15 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76f8f88e81cdfebcab6ff2a9e3fcda513a994fa93b5778482958419f84f6988`  
		Last Modified: Wed, 24 Jul 2024 01:47:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:327ada9f4cd118d52fb95a2e9c5fd867163d92ce4f99e38951946c538b0e7401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1013596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627f6aa617877df545b95cada898f916964b7145ccaace666aea41bad1424e9c`

```dockerfile
```

-	Layers:
	-	`sha256:3758d18dcd007ea48a83bf32d798631c9547315aca7b061391a3279a9447264b`  
		Last Modified: Wed, 24 Jul 2024 01:47:15 GMT  
		Size: 968.7 KB (968717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6163f85d25cadeae0fc598b00d188bdd5c2b8702570e6c66d293c9c9c7a40d3c`  
		Last Modified: Wed, 24 Jul 2024 01:47:14 GMT  
		Size: 44.9 KB (44879 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:9888d24ac39f1b878a393d80f7d639eee474ddd951b6b5bd642e04dde0c787f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100578587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef2637dabab8997cfa6a9cd7b8e90f72754e9c0e75b9f76717e7beafedde494`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=14
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=14.12
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7325a07f3ca6d8d0751558d93bf190c28073c9e0318b18fb0e10f5817e62c20`  
		Last Modified: Mon, 22 Jul 2024 22:15:44 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2126e13c0db4a6e37cae84d05507d1331675a79086457ddc5556051a5862575`  
		Last Modified: Mon, 22 Jul 2024 22:15:44 GMT  
		Size: 1.1 MB (1095469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017f50de8686d096ae16fd14347e270eca6d0b919a38e94702a178f763ce19e3`  
		Last Modified: Mon, 22 Jul 2024 22:15:44 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cdd366cbe8adb78f6f7c93158c627e55fcfadefdef11c78fb7c5b507ead880`  
		Last Modified: Mon, 22 Jul 2024 22:15:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8141620fad4067e7e081d04c59de78df16b286231c2f3e490903b284e1cfa353`  
		Last Modified: Mon, 22 Jul 2024 22:15:48 GMT  
		Size: 96.2 MB (96213867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe24992e201368f68b2ea0b68b5736b6c83c3c971a5dec2a4a3359d291fb26b`  
		Last Modified: Mon, 22 Jul 2024 22:15:45 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e78a71355644027c354eda204e5dab519a24552c64416218e2c30f49eaecf3f`  
		Last Modified: Mon, 22 Jul 2024 22:15:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c325e8d95a9d8bcaa666a9a27e78179879ac8d0bdff8f78ee93eec698d74133b`  
		Last Modified: Mon, 22 Jul 2024 22:15:45 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e088ca13a956eeb34c37843302c2889d5830b0e69a9cd448a1491f6cf69773c`  
		Last Modified: Mon, 22 Jul 2024 22:15:45 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8708f7e7edacf025b07c4ddecc3ab4b3e5560c05e5f6255b19cf0d2d7a4deb0`  
		Last Modified: Mon, 22 Jul 2024 22:15:46 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:bdab4e35fa1b27a706569855faff4af94ec588cf3f92f295662984cd48efac69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1013236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea0c99331bc5b64cccca6792d77193aead85cb78a7f12fcffc35e99db95af18`

```dockerfile
```

-	Layers:
	-	`sha256:54958e78099ecc056a535915d417849e62174e6f2de172cf4d37d1a740431144`  
		Last Modified: Mon, 22 Jul 2024 22:15:44 GMT  
		Size: 968.7 KB (968670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33eb27b25787789b1b1d85bec9533509b377ee5743f771588090fd67c0ccf9e4`  
		Last Modified: Mon, 22 Jul 2024 22:15:44 GMT  
		Size: 44.6 KB (44566 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:b66ab9775ffad12f560357debb294423f7dab47e941b61597c1c314cbb5b7ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99800341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84461dadc71a39572e5fa0dd40684efbe767f8873f71d9a90e72c970b8dc0e45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=14
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=14.12
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330cbbf50ded2e8625229e0d1e3964baec3bd1e5d5ed44264ab099a2b5e848ad`  
		Last Modified: Tue, 23 Jul 2024 23:23:42 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff859a6049bfe7ca7de74b2eba16642ac6dc3d517e4a0e82b8a945e876f9a19`  
		Last Modified: Tue, 23 Jul 2024 23:23:43 GMT  
		Size: 1.0 MB (1039694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4fe8ac10c74e56495df6b59aa5abeabfde6a5e29f97d4f59665314537dbbab`  
		Last Modified: Tue, 23 Jul 2024 23:33:17 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae769bd801e43c04b8598e0cf5b7075888000ea67abea2d20bc80c69eaa5ad85`  
		Last Modified: Tue, 23 Jul 2024 23:33:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42306d47ec13b77386c0429da9dfaea96c9258380d9974325f1f01ec824fd5b`  
		Last Modified: Tue, 23 Jul 2024 23:51:45 GMT  
		Size: 95.4 MB (95380879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcd997d25981e96cff466675b3ec9936b69ab638c7da5334aacb9de06866a57`  
		Last Modified: Tue, 23 Jul 2024 23:51:42 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf96fdccdfd3155733e42220991e91b96aac4a06dd039f698e0586d2d7fced2`  
		Last Modified: Tue, 23 Jul 2024 23:51:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8c716fde6efc7962bce36aef0c760a0aa41f050acbae3c5c42cd64f5795998`  
		Last Modified: Tue, 23 Jul 2024 23:51:42 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930fb22fd79584d96bf5dd732ac4eae49239e92e58f966bc5f0e06bbf7977b38`  
		Last Modified: Tue, 23 Jul 2024 23:51:43 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9a1e0b1087aa47fb335f5f9c2a47df251ae0ef430b05fab161e2b14f4a2653`  
		Last Modified: Tue, 23 Jul 2024 23:51:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:3b214f358f5c0237066a8357a8c9be289f2de743cf371411b4064dafd2a22406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1009733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05e22bdb57cb4ed6e42515d4027d353ec78352bb1ae7d0ac0048c11c871e98a`

```dockerfile
```

-	Layers:
	-	`sha256:3acbeabc603e19ed8d29f0eb2562f280ad085f94a68f414c57aeb719e0a5d1e0`  
		Last Modified: Tue, 23 Jul 2024 23:51:42 GMT  
		Size: 965.1 KB (965089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513da2aa53e6918be38492f485a56b7a1ef6ae319a28de2c34490ec2b4e1d365`  
		Last Modified: Tue, 23 Jul 2024 23:51:42 GMT  
		Size: 44.6 KB (44644 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:f0d858393d3fbe31fcce1c387840261cd3894310e34ca6df457bcd2b153846eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104179670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4e6f110efd51b7f108a4c4afe2cfa9b539abbd566becaa0b539406d5aef85e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Jun 2024 20:57:56 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV GOSU_VERSION=1.17
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV LANG=en_US.utf8
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_MAJOR=14
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_VERSION=14.12
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Mon, 03 Jun 2024 20:57:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 03 Jun 2024 20:57:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 03 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 03 Jun 2024 20:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 03 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGINT
# Mon, 03 Jun 2024 20:57:56 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 03 Jun 2024 20:57:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a29d9d18637c0fb6d9c43edc04cb197f68cc8695789c1b8783e7ec487ee7e1`  
		Last Modified: Wed, 24 Jul 2024 02:29:35 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad71b789841929b348e9494efffad7d755d93cd961944ae2e8763f697e162c9`  
		Last Modified: Wed, 24 Jul 2024 02:29:35 GMT  
		Size: 1.1 MB (1083899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff303435aa88cdece9b5dd2faa434d46a63cda4d2e116304df6de125bdf1a95`  
		Last Modified: Wed, 24 Jul 2024 02:41:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05718277fc1b9b61c11a10cfa85b56974ab1ec3c28091bf8f3eb779c3f94af1b`  
		Last Modified: Wed, 24 Jul 2024 02:41:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc98904283b4747d4b8547edb22eb2b42d834028b8a3e06fb1347b5fd9e2836`  
		Last Modified: Wed, 24 Jul 2024 03:00:36 GMT  
		Size: 99.8 MB (99826030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f96ee44a8c7092976bdb7bfdf5d52144e6aee8428a98f560ae3db03b69f2c85`  
		Last Modified: Wed, 24 Jul 2024 03:00:34 GMT  
		Size: 9.2 KB (9208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb07755873ef50390e82e9173ef8343b2e55a8e261e3fe2dc64e63a636cbb7e`  
		Last Modified: Wed, 24 Jul 2024 03:00:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8764f22e11d8e7ec04c06e5e5851e3a29dbddff62d4d2660e1992f3719a20c0`  
		Last Modified: Wed, 24 Jul 2024 03:00:34 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a1268ff58a11fc157df706d3b86eb2aad90ac3087adf13062490bc716aa680`  
		Last Modified: Wed, 24 Jul 2024 03:00:35 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a9da862bf501d3e815160817d8d69168b3244ca30dcf7d923b8fe94a56fb1a`  
		Last Modified: Wed, 24 Jul 2024 03:00:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:1e21e49801fa4e85ffb2022cc7e3fe845f70ab184b0f0bcb96e51fa2140fbbdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1011334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed666dfeb42e03977e6a789847324e1ad3eeec33b0c3aee7940c41bffee5dd1`

```dockerfile
```

-	Layers:
	-	`sha256:3f0e07bb34bf0bdb53b340eb185a58b7b5af3ea7ef6ec1d6556b6775d3699ddc`  
		Last Modified: Wed, 24 Jul 2024 03:00:34 GMT  
		Size: 966.7 KB (966731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d1ce8af520e3864208b1c90eddeb657577fee61ce88217d0dbfe1ecbcd58852`  
		Last Modified: Wed, 24 Jul 2024 03:00:34 GMT  
		Size: 44.6 KB (44603 bytes)  
		MIME: application/vnd.in-toto+json
