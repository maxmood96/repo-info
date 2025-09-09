## `postgres:18rc1-alpine`

```console
$ docker pull postgres@sha256:8f5522409c5a14af5816b1e3dd7c537de31ea6dd2af300fd37c27613e73258be
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
$ docker pull postgres@sha256:d7b51044945c171956e3bbcf600f3a1d216fb277f8b46585bae9325ca2a1e248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113932761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1552207d4c3fa0616cb8d873fd400f95002f3a8184b9ba2470cf96a334d50fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV LANG=en_US.utf8
# Mon, 08 Sep 2025 20:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_MAJOR=18
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_VERSION=18rc1
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_SHA256=b1a4cdc0ed6e97d117f044da67815829d560002c821290a9dee86e5e499b2f4c
# Mon, 08 Sep 2025 20:04:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
VOLUME [/var/lib/postgresql]
# Mon, 08 Sep 2025 20:04:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 20:04:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Sep 2025 20:04:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3258f17b90277b4f831c93092998b1bfe9e52adfd6be1b998d3c9cbc3f398dc7`  
		Last Modified: Mon, 08 Sep 2025 22:48:55 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378802045a5e5505b8dc30d209ffdaef5e3599d9394044a178aafe7fdcdc9660`  
		Last Modified: Mon, 08 Sep 2025 22:48:55 GMT  
		Size: 914.8 KB (914827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c00ae8eed6da3551691f8d9ebf3c7de1824d802e924298cfae1692137ae7b35`  
		Last Modified: Mon, 08 Sep 2025 22:48:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab79ea3092cc4206faf90f5e788f0099f9e2cb524776dada20d2cff1bfc31aec`  
		Last Modified: Mon, 08 Sep 2025 23:31:39 GMT  
		Size: 109.2 MB (109191958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c3e1c100574dc32099de60da14eee972c9d4ffad36535db0244dd62b7f4234`  
		Last Modified: Mon, 08 Sep 2025 22:48:55 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687f814c0bba816dbcc9b8f219698c5fba24eb775a1320b3eb74a20b44de2a6c`  
		Last Modified: Mon, 08 Sep 2025 22:48:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264e294a0fa1ed859092e1b3e5cdd77511d35b2d9b151c360984d2c5a7ff43ee`  
		Last Modified: Mon, 08 Sep 2025 22:48:55 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25a0fd23cede4b37563db95114da06270cbfdf2c5baf2a85208c64669f5548f`  
		Last Modified: Mon, 08 Sep 2025 22:48:56 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec20004c7b06fde914de3f5beea1bb43c1ead690e98d390076ab80d6c27f402`  
		Last Modified: Mon, 08 Sep 2025 22:48:55 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:6fd6e0aa5bb315a66306cca3bb28cfc8964b38d24a6833940afce4f62715cf64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.7 KB (637660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29024512941f3fce34b83e8daa6bf79635d38db7a2dffb67ff6774a477f30134`

```dockerfile
```

-	Layers:
	-	`sha256:ba88fe48b7901be4d1f735a73323fcd9bef0cce4adc3c44342cb07b270ca1719`  
		Last Modified: Mon, 08 Sep 2025 23:13:42 GMT  
		Size: 596.3 KB (596313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81603d5b16e5db0907ed8a8ba342eea5e1fd46d0077e6166a509d6b46572d15c`  
		Last Modified: Mon, 08 Sep 2025 23:13:42 GMT  
		Size: 41.3 KB (41347 bytes)  
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
$ docker pull postgres@sha256:add542868e50ee52ae80405cdfc737f39ed665a3b0e555e90406247e1e4d3805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120092635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7bf84ffd956e4079b4d4d39de654052aa05a02090d16b6bdaf6217b5a6f2b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV LANG=en_US.utf8
# Mon, 08 Sep 2025 20:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_MAJOR=18
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_VERSION=18rc1
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_SHA256=b1a4cdc0ed6e97d117f044da67815829d560002c821290a9dee86e5e499b2f4c
# Mon, 08 Sep 2025 20:04:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
VOLUME [/var/lib/postgresql]
# Mon, 08 Sep 2025 20:04:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 20:04:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Sep 2025 20:04:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ff13c53a5ae3cfd58346de6dacda8f4ecdc94d9a9ccb8d9658277bd968fc8c`  
		Last Modified: Mon, 08 Sep 2025 22:57:08 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56a4eeaf5e61226e9edb793439768d9715a8951a3a44b4d1ec703ad96d32fd3`  
		Last Modified: Mon, 08 Sep 2025 22:57:01 GMT  
		Size: 885.2 KB (885200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c00ae8eed6da3551691f8d9ebf3c7de1824d802e924298cfae1692137ae7b35`  
		Last Modified: Mon, 08 Sep 2025 22:48:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8a6d3fa37edb3964e54d3079e909117c050e90d39ce16a180c3a1fa8e3a8ac`  
		Last Modified: Mon, 08 Sep 2025 22:56:55 GMT  
		Size: 115.6 MB (115566142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c9b4faf314af4308e6b4c363fb033967b712ceb33e815eb73ee8e0b7b51235`  
		Last Modified: Mon, 08 Sep 2025 22:57:03 GMT  
		Size: 18.8 KB (18776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6523e23b1495d0ef59ce5df80ad991933b7e58db51eee4b39ec6d4c7cc9b5b`  
		Last Modified: Mon, 08 Sep 2025 22:56:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceab861af4ce74139857b56ed4c8a6f7251096f3ba85190b45d15913596b7f91`  
		Last Modified: Mon, 08 Sep 2025 22:57:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf72ac1f0c2627582e86595cd12a877aebbbb3027ecd5665671aa091b08dc2b`  
		Last Modified: Mon, 08 Sep 2025 22:57:10 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03fe9ca96f6b8e5cac7adf8bb53b54be0d2bb669be03a635f83d0947165946d`  
		Last Modified: Mon, 08 Sep 2025 22:57:06 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:1fc3aca754f28f3c9c7fc79b6f619adad850207bf09de34548df256162ab97a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.6 KB (637609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918119809ac1cb00633ff13ad782250cd4e402edf953c3da6333942f0f39e64c`

```dockerfile
```

-	Layers:
	-	`sha256:9a8f20d621b6533db66d7801aec67f64931576d8ac73fc2f6d4414c468a4b5e0`  
		Last Modified: Mon, 08 Sep 2025 23:13:52 GMT  
		Size: 596.3 KB (596298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:919925f5831315f8147689f0147972dd9666a583777cfc6159fc5cf7772c7719`  
		Last Modified: Mon, 08 Sep 2025 23:13:53 GMT  
		Size: 41.3 KB (41311 bytes)  
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
$ docker pull postgres@sha256:6d9b0db51241dfe7573d60653e6fa9d84570f0b926bfb809a9d1140fa2bc8260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113771413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ea0c9b3737d6d40d4323199a4d7409b0ff19c03b3807ae9d327c0a9af25328`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV LANG=en_US.utf8
# Mon, 08 Sep 2025 20:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_MAJOR=18
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_VERSION=18rc1
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_SHA256=b1a4cdc0ed6e97d117f044da67815829d560002c821290a9dee86e5e499b2f4c
# Mon, 08 Sep 2025 20:04:25 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
VOLUME [/var/lib/postgresql]
# Mon, 08 Sep 2025 20:04:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 20:04:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Sep 2025 20:04:25 GMT
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
	-	`sha256:bf4c015cfadf8b69ffbe3e3d53c3e428799504bf10e3d37e9507e16d086df808`  
		Last Modified: Mon, 08 Sep 2025 23:00:00 GMT  
		Size: 859.8 KB (859759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31018e3103a190cc0e4cd7a25580f6b7b3b852348c9be65f8addc1079f86d4ad`  
		Last Modified: Mon, 08 Sep 2025 23:00:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16387e2c56648cdb8ff6cfe029e9359a2373a29379721654556e5e3a0fb65a6a`  
		Last Modified: Mon, 08 Sep 2025 22:50:55 GMT  
		Size: 109.4 MB (109372551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f65c455319e64466c99fb6054a0ad4edaa6ef24a858c1c8a9b92486f48ce693`  
		Last Modified: Mon, 08 Sep 2025 23:00:10 GMT  
		Size: 18.8 KB (18784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e295004cd3ca64c0280cc010cbf677baf1fff135f163def73b3f0527828e95f8`  
		Last Modified: Mon, 08 Sep 2025 23:00:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefeb267c05cd4fd75d07ab4cc5b9747b58766c895cf5960c6c6bf5dc72897e9`  
		Last Modified: Mon, 08 Sep 2025 23:00:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cacab8174d0ff54c941f3fcc2d867558fdfb1a7bc537ec787f8fee59a506e21`  
		Last Modified: Mon, 08 Sep 2025 23:00:20 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0832de75765c6e60ad9c08886a4c5b9be88f02b0f4cfdf05e432259d66bc8003`  
		Last Modified: Mon, 08 Sep 2025 23:00:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:32ba830b0d6e9d7b637f5bbed9ae33c9b63570361c20702a9456e16811d6eeab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.8 KB (635773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ec051585f2734d19ab81f3307e0ad2d0c835566c2b57d6d52568d87daf87e9`

```dockerfile
```

-	Layers:
	-	`sha256:a8edc202e58451ec9c7386a39ed01223b59b7d722e60acfa1da118bc8d8d95ac`  
		Last Modified: Mon, 08 Sep 2025 23:13:59 GMT  
		Size: 594.4 KB (594380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25ff2bd4cad32dd258a12d5cdd6964f9e4fbaf0f153e06dd770c63eeb252d462`  
		Last Modified: Mon, 08 Sep 2025 23:14:00 GMT  
		Size: 41.4 KB (41393 bytes)  
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
