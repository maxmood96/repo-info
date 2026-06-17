## `postgres:19beta1-alpine`

```console
$ docker pull postgres@sha256:66a79a88d852d5b81ab9a82a77acd5738062030e2f5a836f6aef08c3cefa4fca
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
$ docker pull postgres@sha256:d423837d852c344684d6ab09bc1026e494adda2ccbd17b0e242c392cd70ed4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121247242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbeee29dcbb05d4fc3f34dae87bea98dfd228871ccc83dd91f72feac6c7ed9ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:57:22 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:57:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:57:22 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:57:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:57:23 GMT
ENV PG_MAJOR=19
# Tue, 16 Jun 2026 22:57:23 GMT
ENV PG_VERSION=19beta1
# Tue, 16 Jun 2026 22:57:23 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Tue, 16 Jun 2026 22:57:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:02 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:02 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:02 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Tue, 16 Jun 2026 23:00:02 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:02 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:02 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:02 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005ff1942ee486c7acbdd196cb6857859ec853cd7af022762ec9fe7253aee12a`  
		Last Modified: Tue, 16 Jun 2026 23:00:20 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f75ba60c363856dca302ca09a818b007dfc21ac2c2ed1740b64adc1ab90bcfe`  
		Last Modified: Tue, 16 Jun 2026 23:00:21 GMT  
		Size: 900.3 KB (900252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b00ac03c4fa8cfe32af2e3cebf9de1f96789fb66173822cca3cb18fce5775a`  
		Last Modified: Tue, 16 Jun 2026 23:00:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b79cd321c845afc450a5603428bfab77100f5af67b211b7c90ae798a14a21e`  
		Last Modified: Tue, 16 Jun 2026 23:00:23 GMT  
		Size: 116.5 MB (116472094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bf851393176b7bb5a7fc4ce02a2e499aa3693864f5c2ef8b27af3749d113eb`  
		Last Modified: Tue, 16 Jun 2026 23:00:22 GMT  
		Size: 21.0 KB (21007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dc55b6e2c193fabf1d41bcb8b7deb051ad36e162ba1e59d3bcfd99ff2f9cb6`  
		Last Modified: Tue, 16 Jun 2026 23:00:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341e28d138059de4b775a34584b1ea54654bf49d22ca302af10b4901b04dcb5b`  
		Last Modified: Tue, 16 Jun 2026 23:00:23 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c840ec795c1fee76a6055087aacf6993871d401a8b7b28a470bff0ae26e96637`  
		Last Modified: Tue, 16 Jun 2026 23:00:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:91889185b60069a7292a188e7c789a509aa73b0e6405977a1d3ee08529bcefdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.9 KB (655880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c6ea8d3d795694cb1ffcbd5c01d1ccb3425d8d8fb1bad8f801626a862c411`

```dockerfile
```

-	Layers:
	-	`sha256:f1804dc8d29c0d4ea0ccec4383ab0017f96f1561fcab1ec6de781617d093f6fa`  
		Last Modified: Tue, 16 Jun 2026 23:00:20 GMT  
		Size: 616.0 KB (616040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:815f31fcaef2bc92dd214987b5c3e8f84e99f9b42a9c25851dd137901b8a7792`  
		Last Modified: Tue, 16 Jun 2026 23:00:20 GMT  
		Size: 39.8 KB (39840 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:6401486a4cddc09346eda91822f071555c8218e16f7f8d464d149cebbc3017b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 MB (117446270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bccf692d4ee296bf57e51ea2916d14dec7a9071584419f003dd5f15d3d634f19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:27 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:57:30 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:57:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:57:30 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:57:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:57:30 GMT
ENV PG_MAJOR=19
# Tue, 16 Jun 2026 22:57:30 GMT
ENV PG_VERSION=19beta1
# Tue, 16 Jun 2026 22:57:30 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Tue, 16 Jun 2026 22:57:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:29 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:30 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Tue, 16 Jun 2026 23:00:30 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:30 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:30 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25018f469fafccf804bf9e783ac48f87c1aec0163bd1119c1a6166dac72e3cc1`  
		Last Modified: Tue, 16 Jun 2026 23:00:44 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dbe011944959749e7f5f74ee647a20e3ea9acdb3178cb9059af359c3a45af6`  
		Last Modified: Tue, 16 Jun 2026 23:00:44 GMT  
		Size: 864.6 KB (864612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d452e19bc168c2653e01ba8e38feee061a7a86e28a793fdfdc51e78c487acd`  
		Last Modified: Tue, 16 Jun 2026 23:00:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8dcdd39e32183e4cef43c16b1d28c0aca71bb6a53dae330d6249996477982f9`  
		Last Modified: Tue, 16 Jun 2026 23:00:48 GMT  
		Size: 113.0 MB (112999707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1170c11827a5af307b53cd140cd9285d86d3caf61df4a72fb5b48223a27db5c5`  
		Last Modified: Tue, 16 Jun 2026 23:00:45 GMT  
		Size: 21.0 KB (21006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d78aa8cef68f48ed99ccf451d43265e4364a53cdcc78285551508e30486d382`  
		Last Modified: Tue, 16 Jun 2026 23:00:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4309c33e7261299dd9687fa66028e5b3f937e3394199f35ddabc2b313cf2362c`  
		Last Modified: Tue, 16 Jun 2026 23:00:47 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895b168ce594b30f270c78d522a5fcfc397cc762a1164ca71ebe8a3608c66193`  
		Last Modified: Tue, 16 Jun 2026 23:00:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:8010804d36ff7e18b2cb742c09f8ef35dd6559178ef30ee674e90cf9f3c8a3e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 KB (39766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa61103b4b0fe421244bb1192160da3a921a1fd85cd9a3191fbfd7a14b5e667`

```dockerfile
```

-	Layers:
	-	`sha256:27bc13f05b084a86915b12cf0be0c433d35c9ec1382f213b365d311e518751b1`  
		Last Modified: Tue, 16 Jun 2026 23:00:45 GMT  
		Size: 39.8 KB (39766 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:c55430e954b80c3f81fc997a9bf40d0c6196280e9f323ccfc37c42b1d76cb66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (110972242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f75b11129baad3c2d4eb74ebd1e54615af125b3c9fd394b7a2b2fd78866f1d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:57:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:57:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:57:49 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:57:49 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:57:49 GMT
ENV PG_MAJOR=19
# Tue, 16 Jun 2026 22:57:49 GMT
ENV PG_VERSION=19beta1
# Tue, 16 Jun 2026 22:57:49 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Tue, 16 Jun 2026 22:57:49 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:35 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:35 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:35 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Tue, 16 Jun 2026 23:00:35 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:36 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:36 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1060eabb070dd07f2b881a032659f6e0c8c9c1ed52af85f3ee76054eba039e66`  
		Last Modified: Tue, 16 Jun 2026 23:00:49 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc22eff39e8558b403f2f83e1c9e89c543d6da7cd4043e87d6200c5c9dac489`  
		Last Modified: Tue, 16 Jun 2026 23:00:50 GMT  
		Size: 864.6 KB (864631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c0d7b2dda1f4225922b32fedef0728fa1f320cb34a16acdef1c51324f6a741`  
		Last Modified: Tue, 16 Jun 2026 23:00:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffaa61d6ad1b58e826ddf78ce6de6f001f6d068cd0174b2a6346e8ca0244daa`  
		Last Modified: Tue, 16 Jun 2026 23:00:53 GMT  
		Size: 106.8 MB (106818494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29b837b1db1abbf4c2c933badd3e809c293e8920be891e3063a5dba23bdf5a0`  
		Last Modified: Tue, 16 Jun 2026 23:00:51 GMT  
		Size: 21.0 KB (21008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ce4fd65b8961aae87e52a6769292aac89406a27896c1d3b6d5bbe683ad142b`  
		Last Modified: Tue, 16 Jun 2026 23:00:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd816d051e1e8bf1de85c8faa47988bbeec3e4b53bd099db8efb8df87b8f4025`  
		Last Modified: Tue, 16 Jun 2026 23:00:53 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b4c19c9057d0e5009bc8e3c0bc2a5d9f2ec427f486e0004a0204d1b51e2323`  
		Last Modified: Tue, 16 Jun 2026 23:00:59 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:dd4c0ab4c4075c4049148de37e7766831f8dc03fb33e85f0b281ac2ea45c2731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.4 KB (655392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f3a1edb53c5b19cc66c80db67e87a05522ac48c6abb8852713297a827f5330`

```dockerfile
```

-	Layers:
	-	`sha256:e66e683c0251087a09c81556964c3cccb0e3db719ae87ab73f116ba146f05645`  
		Last Modified: Tue, 16 Jun 2026 23:00:51 GMT  
		Size: 615.4 KB (615410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11b910f2ea01e9fada53683bf6d0d3171acf4108eeb156cf5134ba75c2bfbe36`  
		Last Modified: Tue, 16 Jun 2026 23:00:51 GMT  
		Size: 40.0 KB (39982 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:677b0a7d53a61a0f98403bc3a5fc10634569feb8ae4c3ac2fe95c70bd8b4b11d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (119018134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9990e6a80b94012d17b90f912a36114b7565a85cb7fdf5f57c3b01be3e241b29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:10 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:57:13 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:57:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:57:13 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:57:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:57:13 GMT
ENV PG_MAJOR=19
# Tue, 16 Jun 2026 22:57:13 GMT
ENV PG_VERSION=19beta1
# Tue, 16 Jun 2026 22:57:13 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Tue, 16 Jun 2026 22:57:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 22:59:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 22:59:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 22:59:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 22:59:47 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Tue, 16 Jun 2026 22:59:47 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 22:59:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 22:59:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 22:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 22:59:47 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 22:59:47 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 22:59:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f27504671d483ac47f9e943688fbfc9846e2989ec941f01ab5165fe57e995d`  
		Last Modified: Tue, 16 Jun 2026 23:00:03 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f21562b5c648feed7106a46d556761b6b027778dcea8008fb1299e64a3db60`  
		Last Modified: Tue, 16 Jun 2026 23:00:05 GMT  
		Size: 852.3 KB (852278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d55689a15bbb604d14590d14a7afefca7c042e638e22d5c804e96428d15a75c`  
		Last Modified: Tue, 16 Jun 2026 23:00:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d30840e32619fd848555312ecc24a2d5e155eb5d297e062e988f6604673f432`  
		Last Modified: Tue, 16 Jun 2026 23:00:07 GMT  
		Size: 114.0 MB (113954319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cab809f88c28ba54069a9b9124d099df5c486a98f8a0cdc59cc926cfe82f93`  
		Last Modified: Tue, 16 Jun 2026 23:00:05 GMT  
		Size: 21.0 KB (21006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbf8fd8fdc8f62e0bfd130552a80f0aa5039c8905a0a9c4a2d43db1af5ca456`  
		Last Modified: Tue, 16 Jun 2026 23:00:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d4a7b5d963f974dccf13628ad5d9af40e6cd3c84a6851b055ac6b771e0eef5`  
		Last Modified: Tue, 16 Jun 2026 23:00:07 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d91685213cbe1f193b747252cf690d15820d92938b718262466b24d34dc90d`  
		Last Modified: Tue, 16 Jun 2026 23:00:07 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:0ecf3b38f527fd4ef092ad3d2ea9ad94a0004b9912477cb2efde6cad041e4ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.4 KB (655431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b84dfb323c396a2575433950965536eaab34db588ea671d25b8bc91a56d587b`

```dockerfile
```

-	Layers:
	-	`sha256:d0b2a519fe5ff957d9ecfb8b4383be90cf03a46c524b4bb5ed52f4066ae2261e`  
		Last Modified: Tue, 16 Jun 2026 23:00:04 GMT  
		Size: 615.4 KB (615422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a82a65cde56ec46492a69bc1fc25ed7f2c41a8c6a3a74dbaa5258d06df286b34`  
		Last Modified: Tue, 16 Jun 2026 23:00:03 GMT  
		Size: 40.0 KB (40009 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine` - linux; 386

```console
$ docker pull postgres@sha256:bceadc100d664743d9f78a54fc9f0091a9d338cad67463d7711b2992c554f1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128169375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418a941d8a1bebf7020246d9e9a070361badf3127726479fccac9d78485af07b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:27 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:57:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:57:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:57:31 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:57:31 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:57:31 GMT
ENV PG_MAJOR=19
# Tue, 16 Jun 2026 22:57:31 GMT
ENV PG_VERSION=19beta1
# Tue, 16 Jun 2026 22:57:31 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Tue, 16 Jun 2026 22:57:31 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:16 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Tue, 16 Jun 2026 23:00:16 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:16 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:16 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cc9cb4e272f4543040e41b320d4d4e0d929df99bed78115da0c8925ffe5905`  
		Last Modified: Tue, 16 Jun 2026 23:00:32 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5931610318394e6b1d74be413ecbdfd9600b598628d778a1f7bc991aae232f55`  
		Last Modified: Tue, 16 Jun 2026 23:00:36 GMT  
		Size: 868.4 KB (868428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad01cc233480bb5288b948f82e5904f09013524aef8b7ffad3f12ae8cf18738`  
		Last Modified: Tue, 16 Jun 2026 23:00:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0218f1ec31eda8ac8bc7a9cd63fc92a6ae81a8e95a73b6e7cb10c5898994e6b9`  
		Last Modified: Tue, 16 Jun 2026 23:00:35 GMT  
		Size: 123.6 MB (123602300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1890ff5d289f59e5472194e673f0bbe2993bbd87faa8ed7fd940edc5c81e9832`  
		Last Modified: Tue, 16 Jun 2026 23:00:33 GMT  
		Size: 21.0 KB (21005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0704630f59e23d1420419291cb7068f449c019407ee0c6e3744bb5424616179f`  
		Last Modified: Tue, 16 Jun 2026 23:00:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fcbc318c3275f98820817a1a96f3ea4611d34b9656397e6c4cbeda3b5874b5e`  
		Last Modified: Tue, 16 Jun 2026 23:00:36 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d8289cfafcdc0edb1869ea0f19dd63d7aff0276912cd7661ec696ef325d9dd`  
		Last Modified: Tue, 16 Jun 2026 23:00:37 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:1deeff30c067e3f25b7d56e14323cbb00f28929c367a10dc77cb125bc206ef8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.8 KB (655831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a34f5aab3e37ff84dfcfc70bfe1fcea4c1adba67758a46fe7430df7cd19f2a`

```dockerfile
```

-	Layers:
	-	`sha256:f4fbf22347c81a445c1c710bd26963bc3c1f835daa145323d730a9b115935a4b`  
		Last Modified: Tue, 16 Jun 2026 23:00:32 GMT  
		Size: 616.0 KB (616025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74bd248818a53954f96a209983fe656a3392921c3824c2592070c285dc3d4041`  
		Last Modified: Tue, 16 Jun 2026 23:00:32 GMT  
		Size: 39.8 KB (39806 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:cddce1f065ebc3bb75ea8c26046d4507644cf2b4ec73beb9484a9c1897a111fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124310060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af26063514bd229c4396e031ad2d2d082c22bcdc3ad8831d4379f8b7bcbdd0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:15 GMT
ADD alpine-minirootfs-3.24.1-ppc64le.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:15 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:56:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:56:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:56:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:56:29 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:56:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:56:30 GMT
ENV PG_MAJOR=19
# Tue, 16 Jun 2026 22:56:30 GMT
ENV PG_VERSION=19beta1
# Tue, 16 Jun 2026 22:56:30 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Tue, 16 Jun 2026 22:56:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:47 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Tue, 16 Jun 2026 23:00:47 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:00:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:48 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:48 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3ebcdcd395ccee658b9200e4b27d7699e5d6ed9f6c1858dea12781aac519ff59`  
		Last Modified: Sun, 14 Jun 2026 06:46:36 GMT  
		Size: 3.8 MB (3813400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a550c138b135a89330347b3a13776cce136b1e19d05c3e2b10571ce2135769`  
		Last Modified: Tue, 16 Jun 2026 23:01:22 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86fd92e78cd7b0d10ecc0f0da5decbed7534334b833b91ed30473a9d6fcb1f`  
		Last Modified: Tue, 16 Jun 2026 23:01:22 GMT  
		Size: 857.4 KB (857445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f7c2433d0811625666a0f10e6fbc0db707597de61db43eda49dc9457e337f`  
		Last Modified: Tue, 16 Jun 2026 23:01:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9014abb74d31c8bd7b4b3888793b7a3070b62418f5f5f106e3b0dfd77b22f21a`  
		Last Modified: Tue, 16 Jun 2026 23:01:26 GMT  
		Size: 119.6 MB (119610707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fc598d3354ee4f78a92b7785e7df6a78566074d192e0a48d343b7f7871b25c`  
		Last Modified: Tue, 16 Jun 2026 23:01:24 GMT  
		Size: 21.0 KB (21008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2396c3d3aad325f860d840e5b742cfcad0bce25369a13641a2f0c8b567a2941`  
		Last Modified: Tue, 16 Jun 2026 23:01:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef2c2c7df768da927b4b1640ccbba76f11d64a8ea16875d1bf74cb829c9e4d4`  
		Last Modified: Tue, 16 Jun 2026 23:01:24 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279cd1beb3793f73687a8a894d30ecba09f7272c7d6ea427a74ee9c458e461a5`  
		Last Modified: Tue, 16 Jun 2026 23:01:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:78b32e2a257e7f747769d6b0797c62f7041c58df6f3c769fdca66898ea0d81de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 KB (653633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef9f393f3a5f40ace1c5aa415c9d2913311501b45cd41b053e06c828322b35a`

```dockerfile
```

-	Layers:
	-	`sha256:498dd10e8e5d1c5f5abf48423a264780e4ae4a8b7df4f6c5723849a92997069c`  
		Last Modified: Tue, 16 Jun 2026 23:01:22 GMT  
		Size: 613.7 KB (613749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56bd9d8f8ebe9f005adc2e6f9d33ea5f8b4a6f4e02412b5e2d7c69cf550bcef8`  
		Last Modified: Tue, 16 Jun 2026 23:01:22 GMT  
		Size: 39.9 KB (39884 bytes)  
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
$ docker pull postgres@sha256:817a394f89072b7331d376296164010592ee0c347188763d9e5c628e0c2ab21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127829596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaea9a07a27f447ba3afd086d69c7cfb723b618138b02a92180199d92491eb5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:21 GMT
ADD alpine-minirootfs-3.24.1-s390x.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:21 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:56:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:56:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:56:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:56:33 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:56:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:56:33 GMT
ENV PG_MAJOR=19
# Tue, 16 Jun 2026 22:56:33 GMT
ENV PG_VERSION=19beta1
# Tue, 16 Jun 2026 22:56:33 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Tue, 16 Jun 2026 22:56:33 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:01:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:01:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:01:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:01:16 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Tue, 16 Jun 2026 23:01:16 GMT
VOLUME [/var/lib/postgresql]
# Tue, 16 Jun 2026 23:01:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:01:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:01:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:01:16 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:01:16 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:01:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:da43be6afaaa3ec1b607461ce64380942a6d76c3d52cda4337b0770d9a96fa89`  
		Last Modified: Sun, 14 Jun 2026 06:47:25 GMT  
		Size: 3.7 MB (3709320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54189aef720d1b483ae234e3366c5a9f60dc8bf570277e4283104b7666598712`  
		Last Modified: Tue, 16 Jun 2026 23:01:41 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cb31ae79a75d787aced66cfc58f372c8f7c1b2223384668263b211e9f9b051`  
		Last Modified: Tue, 16 Jun 2026 23:01:41 GMT  
		Size: 874.5 KB (874500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb94dbceaff977ea64bcee17d71ca7b9dd648f1e9dc804f4d6489794b73a206c`  
		Last Modified: Tue, 16 Jun 2026 23:01:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484d42fec07d6a25f89e98ec7244cbdac9341ceed220e02c66eb54f99745ba6d`  
		Last Modified: Tue, 16 Jun 2026 23:01:44 GMT  
		Size: 123.2 MB (123217275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89a7c09d3c06308e8b9a25d268e79b54584bee795aa4ff1540f3829ade41769`  
		Last Modified: Tue, 16 Jun 2026 23:01:42 GMT  
		Size: 21.0 KB (21006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72661e615573754692e1025dc60804991c51b57267bb8ec1d4a5f575bf54c1cd`  
		Last Modified: Tue, 16 Jun 2026 23:01:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c227ffbf98e7021f84cfc765d2be71643471795bcea3e6f904cf5cc3f433b3`  
		Last Modified: Tue, 16 Jun 2026 23:01:42 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbf6b56beb6f5f53c19ba1ea301f56fa67227eda39fd77b7beb0c06cfb60921`  
		Last Modified: Tue, 16 Jun 2026 23:01:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:4569f28979bdde9557f250381c5837b47fcdccbdc7b9134eeead92ca2c0d1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.2 KB (655228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d74b862f7e375d7b39dca59ca8f8d148dfec5095083966ecbb0e527548ecfbe`

```dockerfile
```

-	Layers:
	-	`sha256:00992632fb476d0f94e257d717d918bd1d06aac49a87570eedbb69c96860f0a2`  
		Last Modified: Tue, 16 Jun 2026 23:01:41 GMT  
		Size: 615.4 KB (615389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2096062e088a13858358c0c6bed173c130880df7ae099a21f27f094b1af9824d`  
		Last Modified: Tue, 16 Jun 2026 23:01:41 GMT  
		Size: 39.8 KB (39839 bytes)  
		MIME: application/vnd.in-toto+json
