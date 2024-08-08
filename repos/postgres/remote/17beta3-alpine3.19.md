## `postgres:17beta3-alpine3.19`

```console
$ docker pull postgres@sha256:1fe22cfa5087375b5c15ba5fd05a901ca87fe0f4032197b9959b0befea2f636d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm variant v6
	-	unknown; unknown

### `postgres:17beta3-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:5d6502544b62da3f7467b9b6ca9c19af550a53a0decd937551c5f51a27f9b6c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96780531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2588155c7babf619ad09a0ac693ab23031b64bfc065e089427869f9910c3b909`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:22 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 22 Jul 2024 21:49:22 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:34:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_MAJOR=17
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_VERSION=17beta3
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_SHA256=010dfaff9fcca6afa2fd576eea89cdabcefc262aa0ba89a6845eaab4d4b08f71
# Thu, 08 Aug 2024 17:34:59 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:34:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:34:59 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:34:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:34:59 GMT
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
	-	`sha256:21943bc7459562df4e4ae8e8ea69b3ff99c293c0116d815e0b7f530233d4ba1b`  
		Last Modified: Thu, 08 Aug 2024 19:10:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423f1975aeb907abfbef15618966f7a87658caba8114763d2bc6b841a12417b2`  
		Last Modified: Thu, 08 Aug 2024 19:10:23 GMT  
		Size: 92.5 MB (92500997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d220b03958e0101f434c317ca3026884405ad10d1e226ee38e696ee744344a06`  
		Last Modified: Thu, 08 Aug 2024 19:10:20 GMT  
		Size: 9.9 KB (9888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7c550b6e95e79ab98ee4ade81eac634975d41bb5473f5dfbe6bae2b19c041b`  
		Last Modified: Thu, 08 Aug 2024 19:10:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3553a6642cb4c30887c531a8f7ddaf7129641f1da76ceeb3c3e0aee085711522`  
		Last Modified: Thu, 08 Aug 2024 19:10:21 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f62c375d399cc8f48a8fd8f0039a2d2f96a12c75230df241d8b9a9c4bbe855`  
		Last Modified: Thu, 08 Aug 2024 19:10:21 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c655a91763f139b98ab3a80f7f02d7ad694911beceb4af7443a67199327a2b`  
		Last Modified: Thu, 08 Aug 2024 19:10:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:6f45f95470a3a0cf8b7f33336eb66b425c739a51143bd5831d80c24d07bfb810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 KB (42016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d995c2daa61e6798eb2ac34215d1c79a58869b7a29a988f658d678b3fefc647c`

```dockerfile
```

-	Layers:
	-	`sha256:8f79726b28065927a096b9aa5a77f8567f194cff12db951009734e2aea8c234e`  
		Last Modified: Thu, 08 Aug 2024 19:10:20 GMT  
		Size: 42.0 KB (42016 bytes)  
		MIME: application/vnd.in-toto+json
