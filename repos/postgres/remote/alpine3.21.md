## `postgres:alpine3.21`

```console
$ docker pull postgres@sha256:dfef35abb36c74ccceb66be0c4b0ea8c28f7ea0b9313108924007528fae532b8
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

### `postgres:alpine3.21` - linux; amd64

```console
$ docker pull postgres@sha256:cb590fc1dce20f7a4e582f8154fb7dac0b233dfab8a185d400988ddc177e381f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110793373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82afb76b791eef4802136b43c1bc6d527d8981f9e9e8b22853d95001513bfac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_MAJOR=17
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_VERSION=17.6
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Thu, 14 Aug 2025 17:12:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 17:12:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:12:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:12:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5440be6151c4a2e573f8cd1c90235aec5a8962fccc9702eff1d8efd9ea79d817`  
		Last Modified: Thu, 14 Aug 2025 18:24:34 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd27ff1e26e6411b0cf545300ab52a74f212d8c0c84aab8089bf72394148ce1e`  
		Last Modified: Thu, 14 Aug 2025 18:24:35 GMT  
		Size: 1.1 MB (1115522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8bf47818a2c7ed4990a812e0749bfce44135a1771d279c16828f82beab05d5`  
		Last Modified: Thu, 14 Aug 2025 18:23:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13b75665a2843ffdbc1960beefa5d66af60452b743e2ebbf18be5234cbc119f`  
		Last Modified: Thu, 14 Aug 2025 20:17:30 GMT  
		Size: 106.0 MB (106022904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e4a12de66c603939106347b284276fa3ca659f44fd42cfdaa52ea702253d62`  
		Last Modified: Thu, 14 Aug 2025 18:24:37 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619dc2a2b8f2f14269509373fce2dc391f3b58a3b2a92977dfbdae71efdef167`  
		Last Modified: Thu, 14 Aug 2025 18:24:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f41eb1cc789e76e9940ec801e0b78b75ff72d0c5ded6a20aa70f03f9ccb561a`  
		Last Modified: Thu, 14 Aug 2025 18:24:35 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b27715b20a85fc2feb0fbb006db27c49e05abf16c5d604483f866059e8e15ae`  
		Last Modified: Thu, 14 Aug 2025 18:24:34 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0361528c2c44da9fd6542325f30a42caf9f32ea49ca8921156722cff0f1e08be`  
		Last Modified: Thu, 14 Aug 2025 18:24:34 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:10b9027495c4830e9967c303062dec0191caa414f61928dec661ba5e1fd5e469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.4 KB (640352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c7cca7e63095c787fdb5c30f0351ce3aa92e3f88e8ed8f096c4f1d181fa9d7`

```dockerfile
```

-	Layers:
	-	`sha256:67064bd1c72ac732f8cca0450f31ab430121b7cf078118c29acab1dc8e19a6d8`  
		Last Modified: Thu, 14 Aug 2025 20:17:12 GMT  
		Size: 599.0 KB (599002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2fff8c77d0a48e22e22fb8dc8022184af4f6da8d1240cdcb0f66efb2c1bb936`  
		Last Modified: Thu, 14 Aug 2025 20:17:13 GMT  
		Size: 41.4 KB (41350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.21` - linux; arm variant v6

```console
$ docker pull postgres@sha256:b8dbb3d0ca8a1229d4f3f1729a5bdab75356cdb10e54ee46fac16438018801ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90336157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34de17e4f1e0acfa2bebe1d00fcccf24fba81970817575407399bdaabab9561`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_MAJOR=17
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_VERSION=17.6
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Thu, 14 Aug 2025 17:12:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 17:12:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:12:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:12:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c24d3e045a6ae3a2737e134a0660bb67966f1c4c59f473117ca5bfb7f462df`  
		Last Modified: Tue, 15 Jul 2025 22:03:20 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85a4c1614afc683eca7c5ab777456f2ae53dd7e1347e7e75764a6a74abf3b8b`  
		Last Modified: Tue, 15 Jul 2025 22:03:21 GMT  
		Size: 1.1 MB (1083487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5769312ee59aeeaaf29de04675a714c2accdd298581e883e9228f0d01acbd5`  
		Last Modified: Tue, 15 Jul 2025 22:03:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c363b155f094cee3ef516415a9fdf551bb002b2c5cca1ef80e2da4472bf70b60`  
		Last Modified: Thu, 14 Aug 2025 18:36:03 GMT  
		Size: 85.9 MB (85871475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85b12bb039d0c1c83ab4c24a8fa5e58f57e3faaf54b19a294157d550aeac8dd`  
		Last Modified: Thu, 14 Aug 2025 18:35:59 GMT  
		Size: 9.9 KB (9887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4529b80c4018068a824ed7ef6242c0ead5869026d58c0bcbaebb5b6e71a169c`  
		Last Modified: Thu, 14 Aug 2025 18:36:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0daf02edad6f9b063edff297ac86f4328007420b1f7d4002ad1575e7d813a3c8`  
		Last Modified: Thu, 14 Aug 2025 18:36:01 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ff766157cc34bc17f3ccb76a15fe49507115af9729e02105f92ee4b7f1397e`  
		Last Modified: Thu, 14 Aug 2025 18:36:00 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd54ee1184a8aaf14e94b8c53b83fb813105c1c5fb9e27710bfbf6055d1dfd20`  
		Last Modified: Thu, 14 Aug 2025 18:36:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:c079cabd63befd7db383e69390f3d3119e6dd21dc5fef8c448b705dae90c35fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 KB (41289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2230f766535b893e573783caa175363a412d3fd4b1cd2cfef3a0d1607c2fbfa`

```dockerfile
```

-	Layers:
	-	`sha256:164fda290673c925583d66212463ea63e44d6df180b48e287ce982dabf66428a`  
		Last Modified: Thu, 14 Aug 2025 20:17:17 GMT  
		Size: 41.3 KB (41289 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.21` - linux; arm variant v7

```console
$ docker pull postgres@sha256:6fdcafa0a02bbf80f96d4368dbe902f74ff10fe8936f0be7e2c4f7a97009b824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85509758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d660bea267cdf2a76fbeed90a41349cf309bc496405e2675054e13d060d22dcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_MAJOR=17
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_VERSION=17.6
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Thu, 14 Aug 2025 17:12:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 17:12:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:12:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:12:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2479436e58684e2eb112538b475b64df7a6f0cf622c2aca2d7639797003ee3b6`  
		Last Modified: Thu, 14 Aug 2025 18:55:36 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53d6ea01dc2439d65ad9dee1318259d41e82100215755413d0040108baa9fa0`  
		Last Modified: Thu, 14 Aug 2025 18:55:36 GMT  
		Size: 1.1 MB (1083499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2484c46995708880a313a40d6efc71623e4b46787fa33b0f964640642a62a4`  
		Last Modified: Thu, 14 Aug 2025 18:55:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a71d9a6284c22307930933f3b2b7a0489fe6644429559e5928ab6d045a0695`  
		Last Modified: Thu, 14 Aug 2025 19:35:58 GMT  
		Size: 81.3 MB (81312005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d541ce55b8b089289d1c218a5271c4946cef78a315471902f542148a95ef06`  
		Last Modified: Thu, 14 Aug 2025 19:35:53 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e919f9f5394284b8333df9ffbc32922364d7d5e53f2da0080ad4b4032734af`  
		Last Modified: Thu, 14 Aug 2025 19:35:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25d33a9a3d3cc444d38ebff00288b168cd634e3e8db1b6a8465a81531d25964`  
		Last Modified: Thu, 14 Aug 2025 19:35:53 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b3ee5861d3ea842057d8311a8175a6816b70206d0d5e27211216566c89558f`  
		Last Modified: Thu, 14 Aug 2025 19:35:53 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa43966f11b3a26156b666ea6249d5bad71ad4ab01f43ed8af3cf2e1dfa0d6a`  
		Last Modified: Thu, 14 Aug 2025 19:35:55 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:0a9ca26ffcee290aee857802aec431c222527ccd41e07c0e4caea9ca18d7b056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.5 KB (640533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f698b96f5bc484faeca03b940f758ba3776ad5d1c238c377e1f1a8624bd3b6`

```dockerfile
```

-	Layers:
	-	`sha256:5d6bbbc3534383e8f4bd1edf3dce10cba950ee5b8a2d6632f6f676157871c5c9`  
		Last Modified: Thu, 14 Aug 2025 20:17:21 GMT  
		Size: 599.0 KB (599030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f801bacba83729fa7f7823ba1ab4ec29ca2e1305d45627a90414b5c3206644`  
		Last Modified: Thu, 14 Aug 2025 20:17:22 GMT  
		Size: 41.5 KB (41503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:cc7b916171def9da33e79cf682599010a1b73181890354b21689ed780964b43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106668582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d07217254a7e3c280bfc1b8cac0f540d20133a136df9721b92cbba2f8b2c0f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_MAJOR=17
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_VERSION=17.6
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Thu, 14 Aug 2025 17:12:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 17:12:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:12:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:12:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0500e99ece82743454c50a08c0096387587592b762bcd82bde615671de2024a9`  
		Last Modified: Thu, 14 Aug 2025 18:57:34 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e8c3ce0b2d4fdb59659874d9a5099fdfb9996a16960ffb02ad370697f0ff35`  
		Last Modified: Thu, 14 Aug 2025 18:57:34 GMT  
		Size: 1.0 MB (1042486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76501b8a95c3831f648e66e44b5a1d9f68199b39e2d3a296dcd29a940fbe3cf7`  
		Last Modified: Thu, 14 Aug 2025 18:57:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14710ed26c275081340131b818b8579f30eed90183904d78315ef99cbfd45c0b`  
		Last Modified: Thu, 14 Aug 2025 19:06:02 GMT  
		Size: 101.6 MB (101621782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0daacdcee92ccaf2c080854f2d2eb598914a8451074d346b5055cc73aa4d05a`  
		Last Modified: Thu, 14 Aug 2025 19:05:40 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5780c9beef9153dca1cb59d5a2e7da43e4de3511b289371cf84e40832d373d`  
		Last Modified: Thu, 14 Aug 2025 19:05:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfb93e8d9d2c4d11747c0caeabd8d8a19412b5f4258dc13bb4b39cc0b0c8ec4`  
		Last Modified: Thu, 14 Aug 2025 19:05:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1828cec15ae89a0016515a0ce645c20e892faa65e616ae73c513d2d9c3c56fc7`  
		Last Modified: Thu, 14 Aug 2025 19:05:40 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eb676391d7903bcd504699178fc23309cae5040fb106c1e68478c592eb1c54`  
		Last Modified: Thu, 14 Aug 2025 19:05:40 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:8f4bfed944f106cd6c04370c0f59169da6dd87f37cacde3a842eb9606769602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.6 KB (640594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d43d2027f03a3e13423e570f881db966809bca34981f8a6efccd1b7feee744`

```dockerfile
```

-	Layers:
	-	`sha256:469cd72759c475bb3b91b8789d0842a598e843b86c930382aeeec6edc1004627`  
		Last Modified: Thu, 14 Aug 2025 20:17:26 GMT  
		Size: 599.0 KB (599046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dce70e43d53b0dcbe24b34dfb059d5ded9bb960fd9e3dc4692f112f286b0dd71`  
		Last Modified: Thu, 14 Aug 2025 20:17:27 GMT  
		Size: 41.5 KB (41548 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.21` - linux; 386

```console
$ docker pull postgres@sha256:6795702e18476250c888bd0a68bf043ccc509102ed5c33f81841608a7e1b2903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116975253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224dab1aac5f209688534a09c045d5bdfeae183cd4481cfcf7d0ef1a66758d6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_MAJOR=17
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_VERSION=17.6
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Thu, 14 Aug 2025 17:12:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 17:12:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:12:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:12:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59545e616f4fa5e6e39f933203d5fe2b7157ecb50972e81f3eb404c3c906cba1`  
		Last Modified: Thu, 14 Aug 2025 19:25:03 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca51dfda1342f4fc7e846674f738a0394608f281ce2457d82fd0f4403f21467`  
		Last Modified: Thu, 14 Aug 2025 19:24:47 GMT  
		Size: 1.1 MB (1091461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3210426a83e783e1454ebbeda1b9e9ce56716026221cf54b48f6ca7a67fbce8`  
		Last Modified: Thu, 14 Aug 2025 19:24:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43efb89236878c33a9b41ec75919940b8a15441406ecae01b29c49d29b803d71`  
		Last Modified: Thu, 14 Aug 2025 20:42:28 GMT  
		Size: 112.4 MB (112405686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a4f0173dea17a6690dfde4ba92521d1d183d87413d9525e64a968d5898d2fc`  
		Last Modified: Thu, 14 Aug 2025 18:33:52 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce65a260039abac89ffcf85bb23e02d203cfe3673c2b51a6b7f9509dffd219b`  
		Last Modified: Thu, 14 Aug 2025 18:33:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec39483a6545498c18ff3de5a34f78eaa286d144257ed5c18a905b8d7261b5a`  
		Last Modified: Thu, 14 Aug 2025 19:24:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a777953933cc525f8d4447ff9bef2ed72bb100f429b949ff916518b789b1af`  
		Last Modified: Thu, 14 Aug 2025 19:24:45 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28b8f106ad18b560afb33e740d7819553bc42fc7ef9e183a0ad2c3b43812e81`  
		Last Modified: Thu, 14 Aug 2025 19:24:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:315116aaae48b2cc3b0f06b0753c68411ff4c0b204794ee38eb04c292c4cab64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.3 KB (640292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e377166f00883d2c143f5e88eb125df556ba1d1d38ec988d8c52b20991301a51`

```dockerfile
```

-	Layers:
	-	`sha256:4102a465955170084ec7a5d15556bd8c8ea5f1cbd98e896a16c796192106782c`  
		Last Modified: Thu, 14 Aug 2025 20:17:31 GMT  
		Size: 599.0 KB (598982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14b16a7cf95ad278800a20944a5cdcede3a75f4cf18067a8ed6c393ecb44af09`  
		Last Modified: Thu, 14 Aug 2025 20:17:32 GMT  
		Size: 41.3 KB (41310 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.21` - linux; ppc64le

```console
$ docker pull postgres@sha256:4691c9b56b34d6b0f0605ed7a976f6ba17dafb7e34337d2affefd0ff017611df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94589221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b106d3fa927f0091dda2e926fba53a34142072efc838c22a17b86c884aaff715`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_MAJOR=17
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_VERSION=17.6
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PG_SHA256=e0630a3600aea27511715563259ec2111cd5f4353a4b040e0be827f94cd7a8b0
# Thu, 14 Aug 2025 17:12:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 17:12:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 17:12:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:12:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:12:46 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:12:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:12:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8dda28bfc0d36b2cb180c6fd3e6a4cd86ecd59274144d20796a06aa044d95c`  
		Last Modified: Thu, 14 Aug 2025 19:18:59 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ad6b1df0987d63949c70018c4fea86e55f4647d138d50f9d0d6b1a34a79140`  
		Last Modified: Thu, 14 Aug 2025 19:19:02 GMT  
		Size: 1.0 MB (1032144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f883acdcfdea9925463802c04d35cd2dbe39acf42fbef191ff71d83149f30b`  
		Last Modified: Thu, 14 Aug 2025 19:19:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e8ca71cd5fcfcbd431f229bba4ca5483996a505ae87aa3af93dfd64f67bfc9`  
		Last Modified: Thu, 14 Aug 2025 19:20:46 GMT  
		Size: 90.0 MB (89970556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16036f867e44487a36c8bc0b65b9991637764aff80debd4014f296def4498b9`  
		Last Modified: Thu, 14 Aug 2025 19:20:37 GMT  
		Size: 9.9 KB (9892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23a0438218a0c18c12f6257ed4a32b6091350207bdca68e97a42f1a0f2c5a3a`  
		Last Modified: Thu, 14 Aug 2025 19:20:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3544f50c020b32cbcffa52eb36649e97c6aa0f9b274c0787367cde8d2f739f`  
		Last Modified: Thu, 14 Aug 2025 19:20:37 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2af97fbe17c553d5538e3891c2eb6fae90f533ec824e251c0d9009f06c098f`  
		Last Modified: Thu, 14 Aug 2025 19:20:37 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23fd6af89dacb6ae2a4198d5325db124274759786bbcfb4308ad8be9df3b13f`  
		Last Modified: Thu, 14 Aug 2025 19:20:37 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:426ece9c1e3026c0e4d65e37264c7afbce5d322d73aa4f2032bdc1bb2e061ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.8 KB (636814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe12fa06aeb852771211958d6abb133c33e5b316e4a48baf976036c2f0b2079b`

```dockerfile
```

-	Layers:
	-	`sha256:c0f5565d4c95e6aa158b19d98240ffcd6aca69d0d1e3213bc8b6e24cf02890f3`  
		Last Modified: Thu, 14 Aug 2025 20:17:37 GMT  
		Size: 595.4 KB (595417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dac3eaea13da37ae273d2ace9440aba99e1d561989ce895320c1ab126d12835`  
		Last Modified: Thu, 14 Aug 2025 20:17:38 GMT  
		Size: 41.4 KB (41397 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.21` - linux; riscv64

```console
$ docker pull postgres@sha256:efd2dc22fa28f3cd9be4404bb9b79e0010c16dc8571a70231b1ee684f32314d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110896726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d660143d77e4bb197c6ae0661860b387f604b61ac3f89f9b601353f6ed9f46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Jun 2025 18:27:47 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
CMD ["/bin/sh"]
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV LANG=en_US.utf8
# Fri, 06 Jun 2025 18:27:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_MAJOR=17
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_VERSION=17.5
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_SHA256=fcb7ab38e23b264d1902cb25e6adafb4525a6ebcbd015434aeef9eda80f528d8
# Fri, 06 Jun 2025 18:27:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109d3c0f56503ab40c4140d482406fc770090c1cfa210c2d815c27c3258a8846`  
		Last Modified: Thu, 17 Jul 2025 05:47:43 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff15b55dbea7fde51e6fef1d6c983e6787f061f6e664e60be0bed1e73ab2ba1`  
		Last Modified: Thu, 17 Jul 2025 05:47:44 GMT  
		Size: 1.1 MB (1085403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d3c738d93a67acc9b823f9b99c37350d12f5f2ca9149f6cfe4afa6c01a0833`  
		Last Modified: Thu, 17 Jul 2025 05:47:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b1620ff3dc70d04bd360c4aa2912ad29122297ba7a1f93a3134af2e795d33`  
		Last Modified: Thu, 17 Jul 2025 07:39:20 GMT  
		Size: 106.4 MB (106444837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc8fdd0d23f29992cb39102da2f3b5a14608fdab2f7d98aab2c49274986f238`  
		Last Modified: Thu, 17 Jul 2025 07:39:01 GMT  
		Size: 9.9 KB (9892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72469a4b280af1d99c65ab443a47d9dbc543d8d2c33674451901f12ddd2f0353`  
		Last Modified: Thu, 17 Jul 2025 07:39:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d710c686b8eefcce05da1752aa1987a9dfcbd50906370377556b6e9005fefff8`  
		Last Modified: Thu, 17 Jul 2025 07:39:01 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d5ce574a4a2ad596dca3b279c6410f394e61fdbd6c7e9688520c579f80e8cd`  
		Last Modified: Thu, 17 Jul 2025 07:39:01 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615097cb08bae1003cf91cc790ba28c4005e0cd677b88b726beda8c601cd616b`  
		Last Modified: Thu, 17 Jul 2025 07:39:01 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:7772fbe3ad50f58c0fa62d55537c365ffa041ae3fe6099a3eb14b882f2b0edda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.5 KB (638477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642f01fd1697951e4bd0d15526517f2d04896f92ada73ae6769a9ad59939ccc7`

```dockerfile
```

-	Layers:
	-	`sha256:8d8bf9dea595ade386643d4e01637851fe7c5573833f2394144bf61b206aee6c`  
		Last Modified: Thu, 17 Jul 2025 08:08:43 GMT  
		Size: 597.1 KB (597075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5785276c73eca8024c31b5b20a65f423fa1c8ac2ac43b86b33e64359bc4e876f`  
		Last Modified: Thu, 17 Jul 2025 08:08:44 GMT  
		Size: 41.4 KB (41402 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.21` - linux; s390x

```console
$ docker pull postgres@sha256:7f4ab2343f52585e7534d01b532d04ce6f7ca905c5cf1c4501321cdaecb4ca49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119378829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91de0ab291f8d2044dc4508be2a7edae0bfd9b05b16b3dd0d53c201a779c407`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Jun 2025 18:27:47 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
CMD ["/bin/sh"]
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV LANG=en_US.utf8
# Fri, 06 Jun 2025 18:27:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_MAJOR=17
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_VERSION=17.5
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_SHA256=fcb7ab38e23b264d1902cb25e6adafb4525a6ebcbd015434aeef9eda80f528d8
# Fri, 06 Jun 2025 18:27:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08ce6f43a6a5f10e7f4be1ad3b21d953126a6a3fadf3e2748946ca632e9cccb`  
		Last Modified: Tue, 15 Jul 2025 22:02:49 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405b45240bca888a7a97d0169873d3fe563c9899d16570f76b85d85bb758d59f`  
		Last Modified: Tue, 15 Jul 2025 22:02:49 GMT  
		Size: 1.1 MB (1081100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2461363266a22cbd95730c416df140d01b4559da8b795a393e3e11c32b052cf9`  
		Last Modified: Tue, 15 Jul 2025 22:02:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10f3e3a909a25f4247b43e0b362b68d110e13366ba6b337722d0f55a5900a9c`  
		Last Modified: Tue, 15 Jul 2025 22:07:20 GMT  
		Size: 114.8 MB (114818253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6ac3a02a2b3c2ef04aaeabc6aebfa34527e0b33567a15748b7fdf5f9e415c2`  
		Last Modified: Tue, 15 Jul 2025 22:07:15 GMT  
		Size: 9.9 KB (9887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d51b5991d55e73374c776ac57197981e3303be5bc0d874637b03315e078ca7`  
		Last Modified: Tue, 15 Jul 2025 23:20:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0730ac088ad5689e7559a533a694392c63b36353e5da9b76306aa010524fe236`  
		Last Modified: Tue, 15 Jul 2025 22:07:15 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2d9700a7843b7498748e3fb33a230602a6d830592b5af97a66aea62c2d9944`  
		Last Modified: Tue, 15 Jul 2025 22:07:16 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a15b504caf60f38d9747f3eb896f704cfe641535b96e9fb0f22f5acdaf39ea`  
		Last Modified: Tue, 15 Jul 2025 22:07:16 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:bcb7151b8174ce444464beaa9d6e06674898a85a4be74dc6693dc1613886a64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.4 KB (638401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9e92e71dfcb6478decee29c91d7b81af359247bf68ff53bb852cad0d832690`

```dockerfile
```

-	Layers:
	-	`sha256:8be8c2a786ddf787e6b97a1a4c3c81a097990194bb1d36ea6a2564af3296548c`  
		Last Modified: Tue, 15 Jul 2025 23:11:19 GMT  
		Size: 597.1 KB (597051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c415b567e04c9e5ebac045b500da3d87a18123a18364227244cd5a205a7a2a62`  
		Last Modified: Tue, 15 Jul 2025 23:11:20 GMT  
		Size: 41.4 KB (41350 bytes)  
		MIME: application/vnd.in-toto+json
