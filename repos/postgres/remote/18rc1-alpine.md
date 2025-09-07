## `postgres:18rc1-alpine`

```console
$ docker pull postgres@sha256:93e57a123ee6a053fba93f3474b02a6b14fbd8abaca7829a4b859822a17d2bfe
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

### `postgres:18rc1-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:bb1b69b4a9d55a40ee2ff2370c2988079de51b1112a022556831b9147c657ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.1 MB (114133580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520a759444f7107fd0eebdfd2d7e433924da40e897943e9a700f6adaf5603f17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18rc1
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_SHA256=b1a4cdc0ed6e97d117f044da67815829d560002c821290a9dee86e5e499b2f4c
# Fri, 05 Sep 2025 00:02:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e939a19a192c650531da3139a887ff822f34676a3d460ef2c9c73a87bca46e4`  
		Last Modified: Fri, 05 Sep 2025 21:51:51 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ad35dc5873720c99a3a03c67acbbad9b2741fa3afdcdacab1ef08d5bc20b34`  
		Last Modified: Fri, 05 Sep 2025 21:51:51 GMT  
		Size: 1.1 MB (1115588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d55986add5d72e8f0bb05930f45a47c20e9d8562bc662b9b4d20e83bca8bc3`  
		Last Modified: Fri, 05 Sep 2025 21:51:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac08029c9aabadb8541d5fa16f68d939b092c7634b72d83ba985a1152f49bf2`  
		Last Modified: Fri, 05 Sep 2025 21:52:10 GMT  
		Size: 109.2 MB (109192015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14779be7e6e12a7460d1bf4673aa484799d6b631a48d8a1c729b44dd0b18793a`  
		Last Modified: Fri, 05 Sep 2025 21:51:51 GMT  
		Size: 18.8 KB (18776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac129b0969ee6f053a9c676a8aaa3133971a37db2b9b49b4a4a483ea662fd3b8`  
		Last Modified: Fri, 05 Sep 2025 21:51:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057e8c58b5cf544f7a051ed0f3de718d83eecbd1b5addd04cefacb5455d45dce`  
		Last Modified: Fri, 05 Sep 2025 21:51:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ecc922100c1f5669b8e0849c32dd3fa4da7385433a20d1c24fe21d89794028`  
		Last Modified: Fri, 05 Sep 2025 21:51:51 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1baa3e5e90489c726a090c19cf382d2caf33bf8564bbdd4652b2436976290e2`  
		Last Modified: Fri, 05 Sep 2025 21:51:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:616cb26c8350ae86d0439a71d8346c52683475769e863d0384452a7f739ed94c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.7 KB (637671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f64025c612c777dcdbad9aecb850ee0b91c7e3419278069f082a42f04c2a3f8`

```dockerfile
```

-	Layers:
	-	`sha256:08e60c32263b42c99e35144ba6fcbda63a612cc130b8309b38cf52b1ef8950e8`  
		Last Modified: Fri, 05 Sep 2025 23:13:32 GMT  
		Size: 596.3 KB (596317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a5b1c1c119f8fabafd10f1ebb360b855d5c6b55a701341e250cb05e09a939b9`  
		Last Modified: Fri, 05 Sep 2025 23:13:33 GMT  
		Size: 41.4 KB (41354 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:0eeb74020525fa581bf8f4cac1b5c6c4add6456dd485ca699c9a5796b9ea4d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93336586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d517526107237f26a8a2375d73eda62ef586df480c6102034c840797eea5502`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18rc1
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_SHA256=b1a4cdc0ed6e97d117f044da67815829d560002c821290a9dee86e5e499b2f4c
# Fri, 05 Sep 2025 00:02:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9787a20fd77861c5c6e0fe13784c284fcfc70e660968e8d80e397bbc22d4417f`  
		Last Modified: Fri, 05 Sep 2025 21:50:07 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0760a37ff6fe459627b7bcc3a52d0c2f7980c07f4a88f19db00e84e879e443c4`  
		Last Modified: Fri, 05 Sep 2025 21:50:08 GMT  
		Size: 1.1 MB (1083517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3e9c9374516eef6434b3bc9ac4aeb179342a476616c433647f0f79606b328a`  
		Last Modified: Fri, 05 Sep 2025 21:50:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2882383196a54f101207770afe2979087eae950611d5fd24129b5c385e2299`  
		Last Modified: Fri, 05 Sep 2025 21:50:15 GMT  
		Size: 88.7 MB (88725870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eab9eb6f714bd95ae810cd3661d256b99ceefa4af2826fc1b12ffbde8b47d4a`  
		Last Modified: Fri, 05 Sep 2025 21:50:08 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d3b300007e49d447bbdf61268ebcd5928aea91480ca0a67ffbb9666894f5c5`  
		Last Modified: Fri, 05 Sep 2025 21:50:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f87d53f9e31aa96f310936af0ee460899c34673e9c348d916b35a3442f05da6`  
		Last Modified: Fri, 05 Sep 2025 21:50:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e827251bf80dc35261b19afe94785476c3495898b5e3a54da347ba668d6c7e7`  
		Last Modified: Fri, 05 Sep 2025 21:50:09 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25d2a7c6432fca7d29bc12002543ede8fd7dd8773a64ffe47a4c7545b59b686`  
		Last Modified: Fri, 05 Sep 2025 21:50:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:8855016d2016ff0df8a2fa39fc2447eb2b4f99e74e36e7f36f7705f4e27991df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2e85bba104736e36590644affdf5ea325731ab42ba98e3eb3a5e9c5f6fec62`

```dockerfile
```

-	Layers:
	-	`sha256:724faa033687bd546f247b519549b44ca46f49cc27399a8240bbb71132cf9abc`  
		Last Modified: Fri, 05 Sep 2025 23:13:36 GMT  
		Size: 41.3 KB (41289 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:d7904123b1b81cfb59dbb02eaf0210e8a367fff616f9b4759d58df11e8e1e865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88374445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e96c9894f2fb64a56ba9c5b30c0ff5778e765ddd9c94202e6b673c01f85cc18`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18rc1
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_SHA256=b1a4cdc0ed6e97d117f044da67815829d560002c821290a9dee86e5e499b2f4c
# Fri, 05 Sep 2025 00:02:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca85b74bc48a8808e2518c10269e4093b88c9ef5e9a6daeb53be66f7553553bf`  
		Last Modified: Fri, 05 Sep 2025 22:07:57 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e060f58b3849328902a66bbc543fa7097fb8208a4d206d1322599b7b4350479`  
		Last Modified: Fri, 05 Sep 2025 22:07:58 GMT  
		Size: 1.1 MB (1083518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc28fa219b36479d7b259963179ba75c505ecaafbad0889c0fb97c72c03ae59`  
		Last Modified: Fri, 05 Sep 2025 22:07:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e394950f9c0e03d50ad9f71bcf392c0fa5370d2e5616e9478a458a4fa4285a`  
		Last Modified: Fri, 05 Sep 2025 22:08:03 GMT  
		Size: 84.0 MB (84045599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfea04aee87d823317d187702dd663ba2c0c0ced82565df43311115a808e2ad`  
		Last Modified: Fri, 05 Sep 2025 22:07:57 GMT  
		Size: 18.8 KB (18779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8025183d26f505d55781d8c4773139e8c77517ef0f85e70ceb278fc4f9ac3b71`  
		Last Modified: Fri, 05 Sep 2025 22:07:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4ef6881f204bd44e3be265051ede2e69d0aea5e0896c820361231b4b7601c3`  
		Last Modified: Fri, 05 Sep 2025 22:07:59 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de4df83611dd4732e1a2bcff297000409785cb5ebe08c72275e14ea14c7aa9b`  
		Last Modified: Fri, 05 Sep 2025 22:07:59 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c808b01a88f40df687d6413c0ecbe7918b33d879918a242ff3577f58f394eba4`  
		Last Modified: Fri, 05 Sep 2025 22:07:59 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:3922738094bb3423791ae06a2a534341c137dafe1a9e98b78b3fc6e0ee3cf228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 KB (637840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a97a71c2dbbec4ee7d0bb045ea14119ac2000869819242eb9d38d499c34a19`

```dockerfile
```

-	Layers:
	-	`sha256:e86c9b0cfc0c4502f6cf2997ae89ce7c45a3e632a463253c63c33131411c63da`  
		Last Modified: Fri, 05 Sep 2025 23:13:40 GMT  
		Size: 596.3 KB (596337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:605882f6753d77386556eeb76f4f83de10ddb5fed8ec3c55e3a72d1e7c4fd319`  
		Last Modified: Fri, 05 Sep 2025 23:13:41 GMT  
		Size: 41.5 KB (41503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:e4f2302ab07b7c9cc62213770cdb38e4fb5b9449745c112ffbc78194ef5293a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110349322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b2944b8914b3c813ad6067141b11a0c4588dcb8d1c2e88e9efcc0f09eb7ee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18rc1
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_SHA256=b1a4cdc0ed6e97d117f044da67815829d560002c821290a9dee86e5e499b2f4c
# Fri, 05 Sep 2025 00:02:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba20fb9227b86a0294d29dded05f766a3456f382d1c8dcfbdcadbc8bfde0aeb4`  
		Last Modified: Fri, 05 Sep 2025 22:07:00 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627babae6cba1df1c57fbf2c85027e10b78f21abcef389688d4ba31a467b5445`  
		Last Modified: Fri, 05 Sep 2025 22:07:00 GMT  
		Size: 1.0 MB (1042497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb3131a113180ee014aa30b05eacb20aff985d0d2c1f6b719c4b1b7e4e9abfc`  
		Last Modified: Fri, 05 Sep 2025 22:07:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c7d60f6c1b87c23afc2d5620afc94fde9b7e769927dddcaa874c3305f77177`  
		Last Modified: Fri, 05 Sep 2025 22:07:05 GMT  
		Size: 105.1 MB (105149784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f88f3f1de7a600346d0b58e0a3b862586b6aa7b0ea3cdbda19053333e94ce48`  
		Last Modified: Fri, 05 Sep 2025 22:07:00 GMT  
		Size: 18.8 KB (18779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a66fad8d3f311c5763e296087eaea8a834ff5c295be3eeff021d66b8fb3455`  
		Last Modified: Fri, 05 Sep 2025 22:07:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4125f33c0743be4367f792b8613d7c1502d711da96bcd3334f0cd9a4b62747dd`  
		Last Modified: Fri, 05 Sep 2025 22:07:00 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66ce38652d0e9f05a304b196487996a02f1aefb0f412b70b812e15b521db7ff`  
		Last Modified: Fri, 05 Sep 2025 22:07:00 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf592d94ad4bc0751168eef02f9552945936abdaf06d7457488d86c447d08a5a`  
		Last Modified: Fri, 05 Sep 2025 22:07:00 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:17063fe0802462569fd1abaefdd47a19c225617b67d95c4db185f72970a65d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.9 KB (637889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f8582ed4ec25e89cb318502abff418c9d4fe5409c477d05c3b82df262f2374`

```dockerfile
```

-	Layers:
	-	`sha256:63c3b94c09f2ef130145f4406405da454a0dbcad7058e52fdf3fc66a21883a58`  
		Last Modified: Fri, 05 Sep 2025 23:13:45 GMT  
		Size: 596.3 KB (596349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffaf0de8eda73b6381169c8b879111c12b6a4bd05dfed5e39aec7abb82d2a6e4`  
		Last Modified: Fri, 05 Sep 2025 23:13:46 GMT  
		Size: 41.5 KB (41540 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-alpine` - linux; 386

```console
$ docker pull postgres@sha256:fff4ad3b55e44e555a6365ad14006370e43f5f221d17a9be1f9d322855c9f68f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120299231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb52f0787a34ebeb1d8a015b1a6904fcb6d827d0747a432c6cb9016b35e46650`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18rc1
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_SHA256=b1a4cdc0ed6e97d117f044da67815829d560002c821290a9dee86e5e499b2f4c
# Fri, 05 Sep 2025 00:02:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762067b086e9265975615fed53fe17ada0501612bd9c06ffe7af9110aee77f1d`  
		Last Modified: Fri, 05 Sep 2025 21:52:05 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b720d6322cc7f3e562fdb7b27a319fec58987f7e2c27ac8b55fa0ad0f51147ea`  
		Last Modified: Fri, 05 Sep 2025 21:52:05 GMT  
		Size: 1.1 MB (1091508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a80f6135dab0c184a39919d0e68ffb227bfa0f7ee9ba1bca021c6f229a3d50f`  
		Last Modified: Fri, 05 Sep 2025 21:52:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701c838a1c08e86dcf90d791009b5535a70b4ad34cea7a7bb0a9f6916eb24e42`  
		Last Modified: Fri, 05 Sep 2025 21:52:15 GMT  
		Size: 115.6 MB (115566427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d152f8c2436bfbaa223afa32c4827a7cc1e363769614f9adc3a7349c3ea94d56`  
		Last Modified: Fri, 05 Sep 2025 21:52:05 GMT  
		Size: 18.8 KB (18776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faaf4f7e97b82902f77fcdf216266deea670551f70b8d51daba21ae2cda311`  
		Last Modified: Fri, 05 Sep 2025 21:52:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3aa6c1c7a084dc954ce13f3393cc7482fec1f3cc2b10917853a8d3de2d7955e`  
		Last Modified: Fri, 05 Sep 2025 21:52:05 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f6257490e7a666fb4274d934a1cd61a11b9a045470a55cf4ea6cdb5b1914c2`  
		Last Modified: Fri, 05 Sep 2025 21:52:05 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b5b2d211d55a0cab63dd69c8d4c0d1324b60b5f3b87c2d50026f350d7c04ee`  
		Last Modified: Fri, 05 Sep 2025 21:52:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:ec2a15c7d5a138cba001f9b5eb58ec68f3b4b0d76e4b05fb998369d4db1a9b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.6 KB (637621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b16f8de4345d541eb16fbb0b6a2821289b7af67178c2c8118491d66fe2fe8da`

```dockerfile
```

-	Layers:
	-	`sha256:5efb51d60b87c193ae86241f6b286f9e74d23f3adedf797da086f723ecec0ee5`  
		Last Modified: Fri, 05 Sep 2025 23:13:50 GMT  
		Size: 596.3 KB (596302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb20c4ef911d2535ed11ede7bb76b6b3b9d5ee9cb7125bb371a269ef1e251019`  
		Last Modified: Fri, 05 Sep 2025 23:13:51 GMT  
		Size: 41.3 KB (41319 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:5cdb60df0fb85373f83b7b840491c91576fa5fc6ab045f97319de56dcd3718db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97870285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54f69c57cbcebd0203edcde8ca37dff544fa04ba4dd54ba39b3fbf836804ff2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18rc1
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_SHA256=b1a4cdc0ed6e97d117f044da67815829d560002c821290a9dee86e5e499b2f4c
# Fri, 05 Sep 2025 00:02:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c014af95ae3fffde136c7b008be59851ef433f59880ed4093aa77909b51adbe8`  
		Last Modified: Fri, 05 Sep 2025 22:21:46 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0939313a939cc02e7111d95c7a2549c4ae41d8d5066f36fe8d96513aa06e640f`  
		Last Modified: Fri, 05 Sep 2025 22:21:46 GMT  
		Size: 1.0 MB (1032221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367d5605b4ffbdbd4cd95fddcc3eaf1f911ee518722e06e491da959d8bcb78b5`  
		Last Modified: Fri, 05 Sep 2025 22:21:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f651aeb505d312bad5bf2e6fb5ef7e56b9695643e43e1cf4d8868dbe7beca6`  
		Last Modified: Fri, 05 Sep 2025 22:22:17 GMT  
		Size: 93.1 MB (93084657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953cfb4baff40c0b52c85b22c1b94c4621e020d3475fe656a8e1040f1701a295`  
		Last Modified: Fri, 05 Sep 2025 22:21:48 GMT  
		Size: 18.8 KB (18785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823b650f12fa61bae2114397e5c3708299b04e39bef1916a4a16d523099b6969`  
		Last Modified: Fri, 05 Sep 2025 22:21:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ab0e62b41979e877efcbe569d14f1108116ca01542a31a65190811e45c4ba2`  
		Last Modified: Fri, 05 Sep 2025 22:21:47 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3dfb05d2515ecbd0f4a949f09296ede36232988919c8619d04ebf87b1cd833`  
		Last Modified: Fri, 05 Sep 2025 22:21:48 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97cea7fdcd9245afa67c6f1956c455bd02678d6f9c85096f2637f8c4623ecc1`  
		Last Modified: Fri, 05 Sep 2025 22:21:48 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:2ace8d9b3d67f4c2866e03f689362b80df30ed600aef918039ea28e4e6b2f5a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.1 KB (634121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a19c28df618ebc8174439f3132a0a1879c80625044eeb61ae0f2039193bc33a`

```dockerfile
```

-	Layers:
	-	`sha256:49ab9f60cff153b281f00d22f7a0e100aed7451efef7eb78cbfdd9a1b95c5b52`  
		Last Modified: Fri, 05 Sep 2025 23:13:54 GMT  
		Size: 592.7 KB (592726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b88acd4edec5d596f3520dbe058dd54d97aeb2aabd6f34e1fa0b8be8faa215e`  
		Last Modified: Fri, 05 Sep 2025 23:13:55 GMT  
		Size: 41.4 KB (41395 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:1b917e15384aec3a6045866d2cc3c42555ce7dbb06a64f21fb290764e533bb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113997395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2294aaddafc48d307a7572c9d0f71ade772ce1dbd68a32253610cc6f5f73c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18rc1
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_SHA256=b1a4cdc0ed6e97d117f044da67815829d560002c821290a9dee86e5e499b2f4c
# Fri, 05 Sep 2025 00:02:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5724522260b6813e9a3d3ce4e2730f87544cb98af292394155e66eabc9d5549`  
		Last Modified: Sun, 07 Sep 2025 17:35:49 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1d7cea892675774d2db51635f19aa3fafbf41556956b6f05f03a866f572066`  
		Last Modified: Sun, 07 Sep 2025 17:35:50 GMT  
		Size: 1.1 MB (1085432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a197e114d6fa6befa5384d28e49cd793b879fe96983c61168df46d4799e4a624`  
		Last Modified: Sun, 07 Sep 2025 17:35:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f28a0335195cba786c4decc7425bc8dd5a4436ffd517df938eea0bb202e1f14`  
		Last Modified: Sun, 07 Sep 2025 17:36:17 GMT  
		Size: 109.4 MB (109372861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bb02cc89c9a572ce9b60f5a606624ea22284ca8d4f41606696224a1832a1d3`  
		Last Modified: Sun, 07 Sep 2025 17:35:51 GMT  
		Size: 18.8 KB (18783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3fc8f0fe8bdb63bdfce67f5627fb02ad131bb5760b64e16d8dc5a0f6d539cc`  
		Last Modified: Sun, 07 Sep 2025 17:35:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aa93c0e6a921e334d975b8a7a9bcf6977a98c781242fed4914c81a48cda711`  
		Last Modified: Sun, 07 Sep 2025 17:35:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83aad718d2c3db2b464a83b7222c6198ba1492fc3ed9fc509eb61add0d6b14a0`  
		Last Modified: Sun, 07 Sep 2025 17:35:53 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac3808062448190820ed32cabc014dfdc4f6d3c3c421e3ce3fca9f5bae6ff72`  
		Last Modified: Sun, 07 Sep 2025 17:35:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:f77cd9d26366b04f4abca0147376b5751200a4d9f823006b5c9317d6168208fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.8 KB (635785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343cc8a5c859b75f8a560826508d50f957becc033c731a5418df9bdfad78e9ab`

```dockerfile
```

-	Layers:
	-	`sha256:377bfd09b52556363a699340be52a1e12cf72d8f578aed2ca5dbba4cc570249a`  
		Last Modified: Sun, 07 Sep 2025 20:08:54 GMT  
		Size: 594.4 KB (594384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4162a0a89b158bc2c8f51d4b62e96b4765575d6760da38fcd9c4779a543f008`  
		Last Modified: Sun, 07 Sep 2025 20:08:55 GMT  
		Size: 41.4 KB (41401 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:6a5b8a7bbb5076f212efa402ca013e3a0ac71188c670eacb2f79f0c19d210a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122649420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b67d30210e6167631c37c3b863a45a0e0a65ac0e14f915f5c1f76fec02f479e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18rc1
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_SHA256=b1a4cdc0ed6e97d117f044da67815829d560002c821290a9dee86e5e499b2f4c
# Fri, 05 Sep 2025 00:02:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d467101b1c89f21b34f1e5039dcdb47ac43cf291b7f93d673760a3a048a0cb8e`  
		Last Modified: Fri, 05 Sep 2025 22:39:50 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dbe92a927cd0526088a4f1df3ffbbe4769943e35be0fdba0f697ce097e4a28`  
		Last Modified: Fri, 05 Sep 2025 22:39:50 GMT  
		Size: 1.1 MB (1081136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fa50b494835f61cfec3b4273bd27966b063c06bf21d851aa435ee08ae0fdee`  
		Last Modified: Fri, 05 Sep 2025 22:39:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008ddf209bfd5913f1cc41cc47f8924db65c89a94e6c9c2f91bb5f60013ed7ff`  
		Last Modified: Fri, 05 Sep 2025 22:40:01 GMT  
		Size: 117.9 MB (117897024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80bfc2f0f3f73596de00eac8a530b6ef173d0b1f338fd232c2fa239dce83e2b`  
		Last Modified: Fri, 05 Sep 2025 22:39:51 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458e2f0c9c81fb1cbe68373eecbe9e2e26e6ca550e6cfac4e8cb30c1a3ad7dc3`  
		Last Modified: Fri, 05 Sep 2025 22:39:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e93f7a5d0fc9c5a9d9208992306e0c205bf5874a49e7110ba32befb9dee3c6`  
		Last Modified: Fri, 05 Sep 2025 22:39:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b231e10f5da8a81d99544abe752dcba475539393c98c71f8512e41c98c9d69f0`  
		Last Modified: Fri, 05 Sep 2025 22:39:57 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d35e23cedb6c7b9c440579f753e6396efe1f1cfda7089835bff5dc96be4b10b`  
		Last Modified: Fri, 05 Sep 2025 22:39:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:da18bdf481669f79bea1769fbf3da62847ddfb8a31f00ed9c432f09b8d1c0335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.7 KB (635721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6c85490ce402374906f79637940ab82eecb6d328ece88c1f1283e4e655c1a7`

```dockerfile
```

-	Layers:
	-	`sha256:af6e7b142bb8550830796f63fa40a6add67e94f84808c524bf6a4359a2dff8d4`  
		Last Modified: Fri, 05 Sep 2025 23:13:59 GMT  
		Size: 594.4 KB (594366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2c6179d6d3b8a9f2aa27e98584990cf4fa5d129d994b78cdeed88eec89133ba`  
		Last Modified: Fri, 05 Sep 2025 23:14:00 GMT  
		Size: 41.4 KB (41355 bytes)  
		MIME: application/vnd.in-toto+json
