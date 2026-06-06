## `postgres:19beta1-alpine`

```console
$ docker pull postgres@sha256:b8ac02270da4756a188d1bdba5e05d2aab4b6b2db8d4b809ace8607c6815adb7
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

### `postgres:19beta1-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:a34ee2dbb99ee0786d98ee4f81e46fcd97481b997f1629509e12d09c63336db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115311223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d106b16cb32d835125a64e530804cab0a9346e90d9d910b5bb34ebcc384f9b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Sat, 06 Jun 2026 00:20:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:20:27 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:20:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:20:27 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:20:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:20:27 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:20:27 GMT
ENV PG_VERSION=19beta1
# Sat, 06 Jun 2026 00:20:27 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Sat, 06 Jun 2026 00:20:27 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 06 Jun 2026 00:23:02 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:23:02 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:23:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:23:02 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:23:02 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:23:02 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:23:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:23:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:23:02 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:23:02 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:23:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a7b9875af66b14eb9ece6ae750fcfbe6653fbaceaddbab2f00e98129fe8f43`  
		Last Modified: Sat, 06 Jun 2026 00:23:19 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a32539fef30777fb198e36621fdba208bc166816c9eccb57e494ffcb8755cf2`  
		Last Modified: Sat, 06 Jun 2026 00:23:19 GMT  
		Size: 919.1 KB (919052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872e894f682ce77ac3be62baf7ea49d2668c16aa89550a035bdb95859755b138`  
		Last Modified: Sat, 06 Jun 2026 00:23:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fc514b22d69b727d4b7c6d732252b764dbd58a12e1982fb76dbaa16f03475e`  
		Last Modified: Sat, 06 Jun 2026 00:23:22 GMT  
		Size: 110.5 MB (110499484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530347d0d3f0388c20f13ecfc7ee5384d2aa223cc85227aba7e76024f880f0f0`  
		Last Modified: Sat, 06 Jun 2026 00:23:20 GMT  
		Size: 21.0 KB (21002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e108257ce483fd81eac9ef4d93cdd8f4f4ca39efd456813552320cddc964ea`  
		Last Modified: Sat, 06 Jun 2026 00:23:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bc4d8b053fd8a8e8de3689b8d0cb76dd2f99c427bba4063fdfbe69a944968d`  
		Last Modified: Sat, 06 Jun 2026 00:23:21 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7784422d57c503aee9f72e6d5d1abdc0948430e474b667fe2efa6dad6417177`  
		Last Modified: Sat, 06 Jun 2026 00:23:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:afe943d324b7c6d6592ae5cdf52a7aa5946359a13138f7b8dca9da4045b2eb7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **656.0 KB (655954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af494d93ca5c9d0c784c64bb1a8cf7feedd0721424e0ddd0650f84d3f21df4ad`

```dockerfile
```

-	Layers:
	-	`sha256:7d0900c92ffb4e5d2bf0d707bf3c463baf0e89d4caf46dc8bc25ce7f2f301083`  
		Last Modified: Sat, 06 Jun 2026 00:23:19 GMT  
		Size: 616.1 KB (616114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9163cbd641bd4fc339829eb554dd9971fcd7e74e76022c0d1a8083168853119a`  
		Last Modified: Sat, 06 Jun 2026 00:23:19 GMT  
		Size: 39.8 KB (39840 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:058a3a96c744531d6dd7196b66b43f757b51b634a4a6a6451b01073d8b68f5a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94689101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e6c50d86cee9cb6b6eef6a6b0ba2de40051b253d070a863e2e33c90a0ab57d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Sat, 06 Jun 2026 00:25:42 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:25:46 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:25:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:25:46 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:25:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:25:46 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:25:46 GMT
ENV PG_VERSION=19beta1
# Sat, 06 Jun 2026 00:25:46 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Sat, 06 Jun 2026 00:25:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 06 Jun 2026 00:28:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:28:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:28:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:28:39 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:28:39 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:28:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:28:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:28:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:28:39 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:28:39 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:28:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daebb9f5e8f2b6b4f17d8f746ccf3bbc14d1f9b66546752815e2efc0d567ba23`  
		Last Modified: Sat, 06 Jun 2026 00:28:49 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9d9ecffa213523ea6d86d925062910c0ebe39e175d897c3da9045e107d1ce5`  
		Last Modified: Sat, 06 Jun 2026 00:28:49 GMT  
		Size: 887.1 KB (887119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0e5f02f5b7b179c34b25532cd0137d006011fe78681f361790dbea6e40d725`  
		Last Modified: Sat, 06 Jun 2026 00:28:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c55cd8730b68230b04eaebb239dde3b5ea18a2042388c27609e48852bae67f`  
		Last Modified: Sat, 06 Jun 2026 00:28:52 GMT  
		Size: 90.2 MB (90201618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ebca7638a5f901665fe6f6ec5be70d5b82ea2753d2a8de93fe116ba66fbe79`  
		Last Modified: Sat, 06 Jun 2026 00:28:51 GMT  
		Size: 21.0 KB (21005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5dea0de845d285bc392bd3c6534e4e9eb1c93b4727b95ba835fbabb7a7ac724`  
		Last Modified: Sat, 06 Jun 2026 00:28:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8971d4bfa2f6813de4a9ea20565f0c04980cfeaa06358f151f02b11ccc9c96c0`  
		Last Modified: Sat, 06 Jun 2026 00:28:51 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb0f15ed73a2e99f3bba9503fd6129d62ad2fcd0a0e861bbadafec0714dc97f`  
		Last Modified: Sat, 06 Jun 2026 00:28:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:eaf71a90e5b12daf8b245c10a66df31c8670b63beb989fe402e78f9a1996c815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f405afc9ddc5d48437cdf9af20213f0c6c4c6774e5022155cda0668704d60c32`

```dockerfile
```

-	Layers:
	-	`sha256:6c571d80d06acb71ddc6cf1383032e6e5e25c817bf5753987e7f0cc3fc97600e`  
		Last Modified: Sat, 06 Jun 2026 00:28:49 GMT  
		Size: 39.8 KB (39762 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:59e1b77031260209e907c51016c5be7e99842f1dc3650c4bd6a2122b2bece1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89730941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877f80686fd6f8f08fc23f0a4da9e4c4fa3cd1a49b063247c63f6c9cbb3eb6a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Sat, 06 Jun 2026 00:26:59 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:27:03 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:27:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:27:03 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:27:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:27:03 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:27:03 GMT
ENV PG_VERSION=19beta1
# Sat, 06 Jun 2026 00:27:03 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Sat, 06 Jun 2026 00:27:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 06 Jun 2026 00:29:53 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:29:53 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:29:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:29:53 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:29:53 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:29:53 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:29:53 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:29:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:29:53 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:29:53 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:29:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bc99a6c147781e4748cc34a78c351eb623a1baad0e491ba89ebf8071079515`  
		Last Modified: Sat, 06 Jun 2026 00:30:05 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f4f91903d26616325842b0e0977b434d25cb829165e4fe754eb50baf840e13`  
		Last Modified: Sat, 06 Jun 2026 00:30:05 GMT  
		Size: 887.1 KB (887108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd98a33e40641faea17661fa987a0e6d11625916beb11ca63a78eddaa276df52`  
		Last Modified: Sat, 06 Jun 2026 00:30:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c204a960a0cc23f4fd1c3a31911e4302179d4cdac99bbfb83335a14b6b95d5f3`  
		Last Modified: Sat, 06 Jun 2026 00:30:07 GMT  
		Size: 85.5 MB (85532210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f10acd68a5aad40877023661b4f4ec0c61208a5e0a9a8a88899746ce5cf9a2`  
		Last Modified: Sat, 06 Jun 2026 00:30:06 GMT  
		Size: 21.0 KB (21005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6227aa749a950fbad94ad88395bbf095b60afbb2b6d5041b67bc32711cfe82c`  
		Last Modified: Sat, 06 Jun 2026 00:30:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26aacd630174c5a3f54c2d516980595c071a8b97b8c3b331ec4da7bcb90d0293`  
		Last Modified: Sat, 06 Jun 2026 00:30:07 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1159cfdfac45e95816e9f650c756c6476f16127102697ff95ea3008c148b4012`  
		Last Modified: Sat, 06 Jun 2026 00:30:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:95b44a37d82f58174f2483a76b74cf9f7b52a029e2f35f8d52a7fa6e3e03ddde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.5 KB (655461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c5046ab518960aea0bbda4ed8335c2a78785dbb11b2cc95e21a65fea94e6bb`

```dockerfile
```

-	Layers:
	-	`sha256:34f1661b1d2483f9525c772d90a275910bdeccc150b3397f74176ab6991217a0`  
		Last Modified: Sat, 06 Jun 2026 00:30:05 GMT  
		Size: 615.5 KB (615484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1eb8c30a15f18708b38da1f8b2b5c1efc29083ff8c03d3a09d9cb2ee7f74d0b`  
		Last Modified: Sat, 06 Jun 2026 00:30:05 GMT  
		Size: 40.0 KB (39977 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:810b1d658597ab81d19291b58ce2cec8f96178d100ca6c54ece3deb87f540d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113448090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4effc9e784ed55915ce7ad050af402e1bc5c2d302e47b2cad908472b9f8f9ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Sat, 06 Jun 2026 00:21:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:21:50 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:21:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:21:50 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:21:50 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:21:50 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:21:50 GMT
ENV PG_VERSION=19beta1
# Sat, 06 Jun 2026 00:21:50 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Sat, 06 Jun 2026 00:21:50 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 06 Jun 2026 00:24:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:24:12 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:24:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:24:12 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:24:12 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:24:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:24:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:24:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:24:12 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:24:12 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:24:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d177a945db3b2c50d8dfaee84d7d4257f4f3bcba153f99f49b92849d031db`  
		Last Modified: Sat, 06 Jun 2026 00:24:26 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14381a2427e793d6649f94fa23fb89db9e5c62908c154f03e1c99abc9d2dad57`  
		Last Modified: Sat, 06 Jun 2026 00:24:27 GMT  
		Size: 874.7 KB (874712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cad2004c5a07673a4b3a46a648f654051e967ae38103170e73d47c38c46f482`  
		Last Modified: Sat, 06 Jun 2026 00:24:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646d3e6a36b3eb3b395a68b9d6aeecf0b27490cc924db04dfcd8867d66175c81`  
		Last Modified: Sat, 06 Jun 2026 00:24:30 GMT  
		Size: 108.3 MB (108345002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d494bad1fefb0f1928867bb8f707a6e66cf73d2ca82f9eef8829abf461c66b9a`  
		Last Modified: Sat, 06 Jun 2026 00:24:28 GMT  
		Size: 21.0 KB (21006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386a5a5012edfff3ac14415e88ddd58e1b9a24ced93e622fddea252a736504d0`  
		Last Modified: Sat, 06 Jun 2026 00:24:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f2682545d245de61667941d76cde5a347dc78356b4293e6d33eb90b121a32b`  
		Last Modified: Sat, 06 Jun 2026 00:24:28 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8235370a8cab81d36155b41af16ec23a06337c2e6f58d2be471297d417b51e`  
		Last Modified: Sat, 06 Jun 2026 00:24:29 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:f4b8f8e588e9d0bbfd3d6667bf08bb96d4b428711989cab96480ed9cd58bf1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.5 KB (655506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc807d448551031176b840e770c3b09e3128ea6fac884e59c9e01d956b1e6c9`

```dockerfile
```

-	Layers:
	-	`sha256:6be444a7020e1b217d60948526137b7eac8fb53b13de301f9ea4b59c48968a1c`  
		Last Modified: Sat, 06 Jun 2026 00:24:27 GMT  
		Size: 615.5 KB (615496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83a7b09e04e887f6ee4621f13d489728b6f4ed8895ec262f6fe67bbd5d81b3b2`  
		Last Modified: Sat, 06 Jun 2026 00:24:27 GMT  
		Size: 40.0 KB (40010 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine` - linux; 386

```console
$ docker pull postgres@sha256:d63e66616834c0c641b447aa0ea4668342d56f1eb6fee61682ee70ec9e3a3759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121572123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0f3894de786ce3822ca9e8529417604c6dd1483473768352aa6a1758d6df36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Sat, 06 Jun 2026 00:21:26 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:21:29 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:21:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:21:29 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:21:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:21:29 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:21:29 GMT
ENV PG_VERSION=19beta1
# Sat, 06 Jun 2026 00:21:29 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Sat, 06 Jun 2026 00:21:29 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 06 Jun 2026 00:24:21 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:24:21 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:24:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:24:21 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:24:21 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:24:21 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:24:21 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:24:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:24:21 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:24:21 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:24:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b9174f081d57c9b7da353e1c96c86f98a8f5a8cfd5d80da54907a7b2887192`  
		Last Modified: Sat, 06 Jun 2026 00:24:37 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689e226f287ac0e16dd69292fda9e1180a7cd10f8a64069629626147a29b2263`  
		Last Modified: Sat, 06 Jun 2026 00:24:38 GMT  
		Size: 891.6 KB (891645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4314cf89114ea480dbc9e9c07c5a6b48c0c2d027be9593d56e3e01f46b83aadf`  
		Last Modified: Sat, 06 Jun 2026 00:24:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc775fd143a81fccc75c21db87e0a1bc04d82d5f79f3223d80971fa48ac01cd2`  
		Last Modified: Sat, 06 Jun 2026 00:24:41 GMT  
		Size: 117.0 MB (116961536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a26a412c45d22cd6ffbf77acd5b33e3663920c6243df382a95efef0db0bd1f`  
		Last Modified: Sat, 06 Jun 2026 00:24:39 GMT  
		Size: 21.0 KB (21003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073988e813a16bbf7f705f31a5cd523b8336525b6cbbc42e8ad984889a024e11`  
		Last Modified: Sat, 06 Jun 2026 00:24:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1940154260c7b2599919868b228f28b5fface426343f1ea325ab5095ec6b5ddf`  
		Last Modified: Sat, 06 Jun 2026 00:24:40 GMT  
		Size: 6.1 KB (6094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e76fbc7ab188f22320c9dc958bb28a1f061c382f81302c2364c2befea921c40`  
		Last Modified: Sat, 06 Jun 2026 00:24:40 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:26e8aa135810c174cc7ef5ac7d87e77b540e5577b811b250994cb36e8742b26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.9 KB (655905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e39755fcd2c48beb1d6cf049eb0d773380d56b5f8c2ee23336b0d31f8aaae3`

```dockerfile
```

-	Layers:
	-	`sha256:2cf60a2453711999aadc0484410ad9986f6f1aa2495a70e6dc29da1542a45eda`  
		Last Modified: Sat, 06 Jun 2026 00:24:38 GMT  
		Size: 616.1 KB (616099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f181c27b0931720a3812e61f19640fa12647de9bcedae9abcf53cba1695ff1`  
		Last Modified: Sat, 06 Jun 2026 00:24:38 GMT  
		Size: 39.8 KB (39806 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:ad211c5c08026ba89e9c3a1260005021529b889cfd284e326abb4b2b49bd2112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100563140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5896a977d0a34caa1ff090251ffb1eece96a6a4e4ded05c69980695c45a0db3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Sat, 06 Jun 2026 01:07:35 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 01:07:40 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 01:07:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 01:07:40 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 01:07:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 01:07:41 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 01:07:41 GMT
ENV PG_VERSION=19beta1
# Sat, 06 Jun 2026 01:07:41 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Sat, 06 Jun 2026 01:07:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 06 Jun 2026 01:12:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 06 Jun 2026 01:12:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 01:12:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 01:12:05 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 01:12:05 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 01:12:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 01:12:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 01:12:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 01:12:06 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 01:12:06 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 01:12:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c2237a359decc44cc6c59f49bcc9dd911477b4e90ec7153f5143b706a6aa67`  
		Last Modified: Sat, 06 Jun 2026 01:12:37 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8dbff20d2d5dae51dcf6321daba82a5b2407c3c4e75ad5c034dc9e1002e289`  
		Last Modified: Sat, 06 Jun 2026 01:12:37 GMT  
		Size: 880.1 KB (880133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c5f90bd0fef1b1501e2e84ee0db1b7c002dc18ab2d13d4467a6742cbecaf3b`  
		Last Modified: Sat, 06 Jun 2026 01:12:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a6da899d541ba6c7f03fa1a86ad510bfad35e250f347f829e4eade28ab80ee`  
		Last Modified: Sat, 06 Jun 2026 01:12:40 GMT  
		Size: 95.8 MB (95823573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ff5ddad4e371becd6bcd6108ee53655741e4411c7bcb512f5b9f64e4252942`  
		Last Modified: Sat, 06 Jun 2026 01:12:38 GMT  
		Size: 21.0 KB (21008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0698031cb99491cb2085f608a481bdf57d2f26531aa21199b9d1c912f5a7abc6`  
		Last Modified: Sat, 06 Jun 2026 01:12:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade42283ed321e6118de689c7f86a7b25608ad5a6a0725f938295b48c0b5f403`  
		Last Modified: Sat, 06 Jun 2026 01:12:39 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc7b301e63a2a0127a623d6b897f64f9997ce18c201517b33f5ff8a5d85c514`  
		Last Modified: Sat, 06 Jun 2026 01:12:40 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:59e179b30ab33ff3e1c70ec22340366c50a7ae399489fdcb4039b6bc87b57dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.7 KB (653702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4abb4d79ec65d5493cb450940fb93bb094b1fbe145ccf7b32a8eac8865d74738`

```dockerfile
```

-	Layers:
	-	`sha256:7a03c9de4bda1fd4375a23ec56d6bb4899037cec51528892a22d7b0b303b12dd`  
		Last Modified: Sat, 06 Jun 2026 01:12:37 GMT  
		Size: 613.8 KB (613823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d8ac2ea450eb7e268ff4984a08e6f23b5a9c7f910d50a8b4750211e0a4075f`  
		Last Modified: Sat, 06 Jun 2026 01:12:37 GMT  
		Size: 39.9 KB (39879 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:2f5630d1578b9ef3fccc681081a72db68fec60812532f3e8e4f975027b421186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116763446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4185b2f47556fa9eff7c5a2e5e1b04ed38426cd4fabcfe3142df70accbb9091`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Sat, 06 Jun 2026 10:50:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 10:50:28 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 10:50:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 10:50:28 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 10:50:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 10:50:28 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 10:50:28 GMT
ENV PG_VERSION=19beta1
# Sat, 06 Jun 2026 10:50:28 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Sat, 06 Jun 2026 10:50:28 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 06 Jun 2026 11:42:04 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 06 Jun 2026 11:42:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 11:42:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 11:42:05 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 11:42:05 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 11:42:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 11:42:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 11:42:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 11:42:06 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 11:42:06 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 11:42:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7df039f81d0d1157153d6a10d87825ed680c09316ad14754246d92e580683b`  
		Last Modified: Sat, 06 Jun 2026 11:45:03 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2a8c7ef4a7e5db1d384052a59b67dbc6a94ac5b2ba0cdd6cf72d3b6c767784`  
		Last Modified: Sat, 06 Jun 2026 11:45:04 GMT  
		Size: 867.5 KB (867539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8afd435738b3e5c8a24e3e7b16535a142b2da6735e29ec0bd3bd54087e793ea`  
		Last Modified: Sat, 06 Jun 2026 11:45:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10343b79618d279bae769ca805ae925f620f6e48adb52250482aef54a215b1e`  
		Last Modified: Sat, 06 Jun 2026 11:45:21 GMT  
		Size: 112.3 MB (112279729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950e77c4da2ca727e71073dd12ac112cdd16ea58672a8eddc1b0f355d35a2e2c`  
		Last Modified: Sat, 06 Jun 2026 11:45:05 GMT  
		Size: 21.0 KB (21012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad25e0626d1b7cebcd5448c70884b138475f66cc245a787b072676c5fc919720`  
		Last Modified: Sat, 06 Jun 2026 11:45:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df879552b7a39e2b40cf60f7df412ed4796e51ecbc65971256255e905786c60f`  
		Last Modified: Sat, 06 Jun 2026 11:45:05 GMT  
		Size: 6.1 KB (6104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc5adddf8259a918fddfca055ab072528f35fcfff8e2ac022573e1353c47109`  
		Last Modified: Sat, 06 Jun 2026 11:45:07 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:098bd30ab8acf8688b492fc0a0a0d0faedad62d02ec12d64673068ceace90536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.4 KB (655365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c6a7abb84d9ba5b6f10fcb7926b494038e67d00f8e520c07d457976258d713`

```dockerfile
```

-	Layers:
	-	`sha256:fe772b54c913629b98551d286d4386cff182fb74bb916c7471aec76c9521d828`  
		Last Modified: Sat, 06 Jun 2026 11:45:03 GMT  
		Size: 615.5 KB (615481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf6d761d515f52343e2cdbd5bffadfff9ba35479190564c25460f6788031e61`  
		Last Modified: Sat, 06 Jun 2026 11:45:03 GMT  
		Size: 39.9 KB (39884 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:52a634e275ac7b043927649c14e9d45b99e992fe4cc45290a71483289f76a955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123619756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b860ec07d8d013bf95aafe2fceaaab9d1e9a864ba5637b5d350f0166fbb14c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Sat, 06 Jun 2026 00:30:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:30:50 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:30:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:30:50 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:30:50 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:30:50 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:30:50 GMT
ENV PG_VERSION=19beta1
# Sat, 06 Jun 2026 00:30:50 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Sat, 06 Jun 2026 00:30:50 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 06 Jun 2026 00:34:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:34:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:34:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:34:01 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:34:01 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:34:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:34:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:34:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:34:01 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:34:01 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:34:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df90638ef4193e964d1d45274a031e2091554fa7f3030a4d577545033735e8ed`  
		Last Modified: Sat, 06 Jun 2026 00:34:26 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dee11e5d4e31ff7dd19ece3a4a435ce7f8da5f7149e69bcebf8988ceb9544b2`  
		Last Modified: Sat, 06 Jun 2026 00:34:27 GMT  
		Size: 895.8 KB (895800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d6b5585cf62b3eb8289a2df7ca5457bab77e772fd1d3d132fa8af0f9414560`  
		Last Modified: Sat, 06 Jun 2026 00:34:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26be43e2acdcb6b38767377658dccc3c1047e950de03cc2c353c6503aaec10e2`  
		Last Modified: Sat, 06 Jun 2026 00:34:29 GMT  
		Size: 119.0 MB (118968921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806caaad758793d4e0993bccc030831db460679db6bdc78aea08fe4d2a94801f`  
		Last Modified: Sat, 06 Jun 2026 00:34:28 GMT  
		Size: 21.0 KB (21006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1f26901788910ac55f4dd14b5090dcd6bad49537c6eeccea12222b82541b85`  
		Last Modified: Sat, 06 Jun 2026 00:34:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb17e10a099b3ca5a93c0cb99f2166fb4e41fc8a12257b4422297d9f932c94d4`  
		Last Modified: Sat, 06 Jun 2026 00:34:28 GMT  
		Size: 6.1 KB (6094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f53bedaeccf8658289445b8cd6bbf3e99c7ca3401fc6f3e141025faf35337d1`  
		Last Modified: Sat, 06 Jun 2026 00:34:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:2dfd3d9ad6990f73c671b6715da1b049b7e902a9e0908cc824941b0150bae796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.3 KB (655303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec58ddbec84dfcd702a9abd75b1afb53aaa9fd4091b10a6c68dc14ab05a1a1d`

```dockerfile
```

-	Layers:
	-	`sha256:66af86627f2c0b03d0733ec81c93845a54a6516ce09b42fe0ddbb55c8bbb209d`  
		Last Modified: Sat, 06 Jun 2026 00:34:27 GMT  
		Size: 615.5 KB (615463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c851e4aa6c6cf125bbedc5706643fef61ec221119c179076b28ba20799de851`  
		Last Modified: Sat, 06 Jun 2026 00:34:27 GMT  
		Size: 39.8 KB (39840 bytes)  
		MIME: application/vnd.in-toto+json
