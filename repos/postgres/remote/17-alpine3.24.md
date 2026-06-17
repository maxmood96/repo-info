## `postgres:17-alpine3.24`

```console
$ docker pull postgres@sha256:90459fa35eba2d988abdf91f24edf41cee96465b279f1785df5d7e07f471f1b9
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

### `postgres:17-alpine3.24` - linux; amd64

```console
$ docker pull postgres@sha256:0a8a1e76503c091f0feb387d51b10fcd746c2d61cf6cdd6e8356973a45e40a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117144034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126edd17cd7e5566fd560e85e256fcb8e58a6db96805a96a33127c535d09f2d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:58:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:58:11 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:58:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:58:11 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:58:11 GMT
ENV PG_MAJOR=17
# Tue, 16 Jun 2026 22:58:11 GMT
ENV PG_VERSION=17.10
# Tue, 16 Jun 2026 22:58:11 GMT
ENV PG_SHA256=078a03516dcdbdb705fecaf415ea3d13a956c589e46f09fed68a06fb00598c90
# Tue, 16 Jun 2026 22:58:11 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:42 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:42 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:00:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:00:42 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:00:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:42 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:42 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ed82280150f29ecbd49b2dd46f7f9e7eb37270e65bfc6100ff44ef6da1c7e1`  
		Last Modified: Tue, 16 Jun 2026 23:01:00 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b04ef97247accfb6f43003d5aee2927b6891f1ca334523774b43c64f069b391`  
		Last Modified: Tue, 16 Jun 2026 23:01:01 GMT  
		Size: 900.2 KB (900248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3ac63fd40d688ca6d987d56b0c009cf0d8b88667270cb0973cc433998cf41a`  
		Last Modified: Tue, 16 Jun 2026 23:01:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9897515a65fa07b6a860e3ec29f691015d99a9f228e00987f0a65307a966cfcb`  
		Last Modified: Tue, 16 Jun 2026 23:01:05 GMT  
		Size: 112.4 MB (112379774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ffff7f7e5e7c2dbcccfccb89cb31e6b7f354ac1ceb7ad9f6bba8c5ec72c668`  
		Last Modified: Tue, 16 Jun 2026 23:01:06 GMT  
		Size: 10.0 KB (9953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826009835b7ee8866a440e282310141207b2f7bd92950b2e77fed00866ab3136`  
		Last Modified: Tue, 16 Jun 2026 23:01:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0815533242b4dfe222f203cfe4b48bbfe0a99156a0e902fa9feb64810f808034`  
		Last Modified: Tue, 16 Jun 2026 23:01:02 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3271cf15ea308512df69eb0994c12ad7d34166d6f7c5b0a1a5573c89d1f13e2e`  
		Last Modified: Tue, 16 Jun 2026 23:01:03 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8274b4c011463ad07ca930ee3e4caea51a28fb8ffb0fd9768553727035b2e1e5`  
		Last Modified: Tue, 16 Jun 2026 23:01:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:9ed1206e532e144460bb99ec0a3eca1f3628249d1e9e1f11bee0d13a903d6353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.7 KB (639721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b4c5280037c9b95791920818cc95d47a6b7c9d0a7aac657261037a5c99b6bc`

```dockerfile
```

-	Layers:
	-	`sha256:1e7b994d4c08a8b24ff973ad4db042f183c1a5b553874c15590092c1a3fef912`  
		Last Modified: Tue, 16 Jun 2026 23:01:01 GMT  
		Size: 598.0 KB (598034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d94d9809a199d5fff2ea8b0bd11cf53c1a796964e572fb8792b5e7bf6931f8bd`  
		Last Modified: Tue, 16 Jun 2026 23:00:59 GMT  
		Size: 41.7 KB (41687 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.24` - linux; arm variant v6

```console
$ docker pull postgres@sha256:1902911d4ca21b4ec0c6b64f08f6c62d630be0fbc7e1055e8e99a87322dc2f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113332243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c7e093dda9851ca4b2432b8b5b4aa5a617e6d81cb5d505e24042a76446e276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:25 GMT
ADD alpine-minirootfs-3.24.1-armhf.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 23:01:00 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 23:01:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 23:01:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 23:01:04 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 23:01:04 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 23:01:04 GMT
ENV PG_MAJOR=17
# Tue, 16 Jun 2026 23:01:04 GMT
ENV PG_VERSION=17.10
# Tue, 16 Jun 2026 23:01:04 GMT
ENV PG_SHA256=078a03516dcdbdb705fecaf415ea3d13a956c589e46f09fed68a06fb00598c90
# Tue, 16 Jun 2026 23:01:04 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:04:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:04:12 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:04:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:04:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:04:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:04:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:04:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:04:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:04:13 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:04:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:04:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3c4836a46d600cfe9a422adf7a80205cb534097e6213325e0176c51f6e5cc02e`  
		Last Modified: Sun, 14 Jun 2026 06:44:57 GMT  
		Size: 3.6 MB (3553450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5b98cdfe66806f1cbe8e9687fb417bb914524e38fbec4595697412b19eeb38`  
		Last Modified: Tue, 16 Jun 2026 23:04:25 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bf9b35de58487a92c576ca1478a6163b8d05963350a7c82feb46c33b4cb4e0`  
		Last Modified: Tue, 16 Jun 2026 23:04:25 GMT  
		Size: 864.6 KB (864618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ff46df890d4a605618b02d78a12c0886e73c866c27966f53b0ac391c06edf7`  
		Last Modified: Tue, 16 Jun 2026 23:04:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e076259602399b70f417da0b40208b66ec39e3e82b85007b0ef8aa35dd0541c5`  
		Last Modified: Tue, 16 Jun 2026 23:04:28 GMT  
		Size: 108.9 MB (108896555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ec215209d7ef6a11f5133b8a9f33d6aaf8f40311c6eaafabf90f0eb5933d12`  
		Last Modified: Tue, 16 Jun 2026 23:04:27 GMT  
		Size: 10.0 KB (9951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45deeed9536a9ea1396e629796ac00b06d12587bf94bd26927ae695f4975960d`  
		Last Modified: Tue, 16 Jun 2026 23:04:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94af4fb77ae7f8d45b3a80a8504210b8efac88f435e0861293b4a17070904b53`  
		Last Modified: Tue, 16 Jun 2026 23:04:27 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa60fb4c4d342ae8d621beef76e7448c142e7e997dc6f6986e29c5b40f1b6f1a`  
		Last Modified: Tue, 16 Jun 2026 23:04:28 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb92cdbe731bb0e32b2fc3d6f697e2a12a3a9cfa68872b34cf23d0cc2a012f3`  
		Last Modified: Tue, 16 Jun 2026 23:04:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:5662f4900a0bcda374e7c26b1efe403e5b3199f944dc72114d044e4a2e361561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 KB (41643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4fadbcc60286b810aeb9f014a86252ce0691c70c2e4d7773ec084f2b89364d1`

```dockerfile
```

-	Layers:
	-	`sha256:4e7b285e30f189dcdcd494ea3831cf3b9a25d957c209e918d45073a34ecd350c`  
		Last Modified: Tue, 16 Jun 2026 23:04:25 GMT  
		Size: 41.6 KB (41643 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.24` - linux; arm variant v7

```console
$ docker pull postgres@sha256:85a340a1a6fba957d0b62440789ee8918e2b688017a5725ee02de0a3b6638f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 MB (107013969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb02649a995f6cb4a481a5df21febbcc5c486eb95556d02282908fe950566a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:00:26 GMT
ADD alpine-minirootfs-3.24.1-armv7.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:58:00 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:58:02 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:58:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:58:02 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:58:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:58:02 GMT
ENV PG_MAJOR=17
# Tue, 16 Jun 2026 22:58:02 GMT
ENV PG_VERSION=17.10
# Tue, 16 Jun 2026 22:58:02 GMT
ENV PG_SHA256=078a03516dcdbdb705fecaf415ea3d13a956c589e46f09fed68a06fb00598c90
# Tue, 16 Jun 2026 22:58:02 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:01:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:01:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:01:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:01:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:01:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:01:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:01:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:01:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:01:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:01:13 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:01:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:01:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bc03a9e5b4dd452551f246e199537fe7afc1765f53f510bc81d26df9845e4008`  
		Last Modified: Sun, 14 Jun 2026 06:45:22 GMT  
		Size: 3.3 MB (3260615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7602c1a5bae583a7a8a84bbf80752c6b482480d07c4b1de2223bb923c1ecfd8`  
		Last Modified: Tue, 16 Jun 2026 23:01:27 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07a5cff0d75cdb7daeb7143fedb3627d92a192e3c14035aad1a0b352fb5b011`  
		Last Modified: Tue, 16 Jun 2026 23:01:28 GMT  
		Size: 864.6 KB (864629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248a64a1f5790f4c876b0a63ce2bd0e70f05f12ed182b592a4a43411c54d65c1`  
		Last Modified: Tue, 16 Jun 2026 23:00:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f7c1f5f725a548a656a108d010698b62a72ef8fe4291456770a2058d25758c`  
		Last Modified: Tue, 16 Jun 2026 23:01:31 GMT  
		Size: 102.9 MB (102871115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1022d6cf5de7b80471e98e903e80b5b34d3bfec11f7b4b6a66ecd1164f4e577f`  
		Last Modified: Tue, 16 Jun 2026 23:01:29 GMT  
		Size: 10.0 KB (9951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1322e7f805902652d14c9dac72097f66edc250cadac8c47fd55188d804f3e2e9`  
		Last Modified: Tue, 16 Jun 2026 23:01:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a03bcd353cac2fafaf46edffda8f17a0035a6bec865b1ebb490c041c4d3ab8`  
		Last Modified: Tue, 16 Jun 2026 23:01:29 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d5bcfb625d36f046324a3f32753ec8057f189b4a6d2b71984bc8e48ad3c534`  
		Last Modified: Tue, 16 Jun 2026 23:01:30 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1c22d345b3344ec50e1c137c1e669f66e4fa0d609c24896231645e2d283d0c`  
		Last Modified: Tue, 16 Jun 2026 23:01:30 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:ce2d4dff4239477db7718586a7611f4ab2d2ae9e0d778462dadc0e33733ed1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.3 KB (639277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf0fa9b2147a97eac1de99d9d68f068efa1ef91167fd26f210007eb78bd41de`

```dockerfile
```

-	Layers:
	-	`sha256:d2fcc682671cb0b063b661df3747762f956f12243eeb0451784911ff03cecce6`  
		Last Modified: Tue, 16 Jun 2026 23:01:27 GMT  
		Size: 597.4 KB (597420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf3a4d88f5893133dff0e2b0883527ba519cf6297a6b26fa639a4d8521afc42a`  
		Last Modified: Tue, 16 Jun 2026 23:01:27 GMT  
		Size: 41.9 KB (41857 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:f6d4c02e92bcfa6a4181a0c0fc7f74c6b5c935cec1bbb16a34e61761012f673e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (114959040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db836939fe3760739047801b3e588e97c8774d02807db98d6e977ec6a5e54a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:57:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:57:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:57:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:57:51 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:57:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:57:51 GMT
ENV PG_MAJOR=17
# Tue, 16 Jun 2026 22:57:51 GMT
ENV PG_VERSION=17.10
# Tue, 16 Jun 2026 22:57:51 GMT
ENV PG_SHA256=078a03516dcdbdb705fecaf415ea3d13a956c589e46f09fed68a06fb00598c90
# Tue, 16 Jun 2026 22:57:51 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:00:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:00:24 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:00:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:00:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:00:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:00:25 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:00:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:00:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:00:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:00:25 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:00:25 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:00:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6579a911b088f858c56926e9b191bc465c01a8f060a8f0608a62a613b2e4f56`  
		Last Modified: Tue, 16 Jun 2026 23:00:40 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb6bc1e12be409bab301178a45ac58b1f1abf5e0452f0456902fc1c3146bbc9`  
		Last Modified: Tue, 16 Jun 2026 23:00:42 GMT  
		Size: 852.3 KB (852276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e03104204f36c5392b5b45abbb317c71bde4dc9ae651a33b930288cf56f4632`  
		Last Modified: Tue, 16 Jun 2026 23:00:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10aee181f9868b360ddf78501ab660aed76698b4a2dfb394ef2500a9788be739`  
		Last Modified: Tue, 16 Jun 2026 23:00:44 GMT  
		Size: 109.9 MB (109906111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b503a9ce4a53006d897148ee6c2e499a14705ea34370332a24d7a35dd9b60`  
		Last Modified: Tue, 16 Jun 2026 23:00:42 GMT  
		Size: 9.9 KB (9950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62462d13b95091a4cfadc09e8fee4d0d4d168aea69fc34ef091588cba37aed6`  
		Last Modified: Tue, 16 Jun 2026 23:00:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ca78e28a266c77e8c720f39ff47dccc7349fb1c7ed877c73c4b520985cf744`  
		Last Modified: Tue, 16 Jun 2026 23:00:43 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff7208b41a1812e0ec65dc94c6ab5221ea9c4cb5354317aa891a36431312706`  
		Last Modified: Tue, 16 Jun 2026 23:00:44 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc038402d188e4cb3b20fb007bc74c586da3aab8be3c0ed5007c9eb45fe60ad9`  
		Last Modified: Tue, 16 Jun 2026 23:00:45 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:cb8021c043ad78f75d493805ec50b67bf1963ad80faa21a640def7871d4d03d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.3 KB (639335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c7b1e0cbeb4300d0cfb2689b21627dc995b2c117c4a1c99154a79042222cdf`

```dockerfile
```

-	Layers:
	-	`sha256:f83dd5b10b73aa68e8b282f563d055c5fb5519e4186e5b8c6b6fb4ac247c0d82`  
		Last Modified: Tue, 16 Jun 2026 23:00:41 GMT  
		Size: 597.4 KB (597440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe4bebf5cdd1699c05633d505f48f4bfeabacff2d277a9a85cca91bfb59b4e4`  
		Last Modified: Tue, 16 Jun 2026 23:00:40 GMT  
		Size: 41.9 KB (41895 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.24` - linux; 386

```console
$ docker pull postgres@sha256:8451627dafa5069537008d8b7b1849b937886fa1a97be149f931bfda022edc29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123832888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64de6e733e7d3d2d114cc7b17903214cddbeea688da46c7414a30d1973b9f55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:19 GMT
ADD alpine-minirootfs-3.24.1-x86.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 22:58:29 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 16 Jun 2026 22:58:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 16 Jun 2026 22:58:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 16 Jun 2026 22:58:32 GMT
ENV LANG=en_US.utf8
# Tue, 16 Jun 2026 22:58:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 16 Jun 2026 22:58:33 GMT
ENV PG_MAJOR=17
# Tue, 16 Jun 2026 22:58:33 GMT
ENV PG_VERSION=17.10
# Tue, 16 Jun 2026 22:58:33 GMT
ENV PG_SHA256=078a03516dcdbdb705fecaf415ea3d13a956c589e46f09fed68a06fb00598c90
# Tue, 16 Jun 2026 22:58:33 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:01:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:01:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:01:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:01:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:01:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:01:17 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:01:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:01:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:01:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:01:17 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:01:17 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:01:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f86df9d778509895efbf9363d8fcb0cbe0b772de536c7218e4c4c947f0be879f`  
		Last Modified: Sun, 14 Jun 2026 06:45:46 GMT  
		Size: 3.7 MB (3670141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7872e5f75739c17f8ec3ef7e5501d1d47fe9094cf589abcacef9e6f177a6c72`  
		Last Modified: Tue, 16 Jun 2026 23:01:34 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d656c4e6d750817cabaf073cf24c98f38e870f5643b635e078620df0e6912e5`  
		Last Modified: Tue, 16 Jun 2026 23:01:34 GMT  
		Size: 868.4 KB (868438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3780a74ccd62a307908bf2fff2478c755a5cd4381c6be1546b1be83f45749972`  
		Last Modified: Tue, 16 Jun 2026 23:01:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3598a5593e97f47be2d878b634db9260e903090f4e84a914112154e4313cc38e`  
		Last Modified: Tue, 16 Jun 2026 23:01:37 GMT  
		Size: 119.3 MB (119276685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a5fb602b72e7cc8a9248ae396d05f1810a8225543fc3d193e051ced5abe481`  
		Last Modified: Tue, 16 Jun 2026 23:01:35 GMT  
		Size: 10.0 KB (9954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3def601e454f511b20cadd81d461d5328ecf1abdc92501692d927cb1bc1fb18`  
		Last Modified: Tue, 16 Jun 2026 23:01:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae80971b03af4f5473f0bb7ced57f611ac63f359d5b2694a1191d79efd638e9`  
		Last Modified: Tue, 16 Jun 2026 23:01:35 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf8bc30a94984aa9e11e49fe2535462ade3c411cdf13ed99c5804a9c90fc05f`  
		Last Modified: Tue, 16 Jun 2026 23:01:36 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadf3ad34333b89057ca9b5ce02cd51a8af9fdca579a91377d983522e1a717f0`  
		Last Modified: Tue, 16 Jun 2026 23:01:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:b2fb9ce1628f5634c6e0a99be6ed2d34cac3924ed2ffed26c1e45b74c45f300c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.6 KB (639650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041e874ddb618566742a08288c10ff840579599fc52bd721239d552d209e33bb`

```dockerfile
```

-	Layers:
	-	`sha256:571e9585514269e73f9d83642e9992e3477e2fe82bd87f2240e47685b0b0ab81`  
		Last Modified: Tue, 16 Jun 2026 23:01:34 GMT  
		Size: 598.0 KB (598009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:350a596b94ffb88fb853b443cd590d072228bbd276e8fb3c0810c1f1a18245bd`  
		Last Modified: Tue, 16 Jun 2026 23:01:34 GMT  
		Size: 41.6 KB (41641 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.24` - linux; ppc64le

```console
$ docker pull postgres@sha256:711fbe220f8c8a62ae9cc1e1c329f791253f78df407dd2c4f673e471e99b3da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119892694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87eb99a9c79665731e16240c35d1631730b531723d4a7d16946fe0929141dce4`
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
ENV PG_MAJOR=17
# Tue, 16 Jun 2026 22:56:30 GMT
ENV PG_VERSION=17.10
# Tue, 16 Jun 2026 22:56:30 GMT
ENV PG_SHA256=078a03516dcdbdb705fecaf415ea3d13a956c589e46f09fed68a06fb00598c90
# Tue, 16 Jun 2026 22:56:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:11:26 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:11:27 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:11:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:11:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:11:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:11:28 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:11:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:11:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:11:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:11:29 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:11:29 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:11:29 GMT
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
	-	`sha256:88064d7f9e003befd8ddc6c8466b4ec215b91d809b77fad8395301bd3fd120c8`  
		Last Modified: Tue, 16 Jun 2026 23:12:06 GMT  
		Size: 115.2 MB (115204224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cb896667fbbdbbb6e525a14f10050ff62af8092477718ac40b274c8147a4f4`  
		Last Modified: Tue, 16 Jun 2026 23:12:03 GMT  
		Size: 10.0 KB (9956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e12a763af8cf42ff7022e1b64b5b93ebd526b14fcff75d9655f017e99a49b4`  
		Last Modified: Tue, 16 Jun 2026 23:12:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232879053f9c675d2671599d1c980dcce170536f3d811fb4b65714f6667dbb48`  
		Last Modified: Tue, 16 Jun 2026 23:12:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c255ec8c776b3fec732064447d4cf56667d5e69ed822764fb29d9177da672adb`  
		Last Modified: Tue, 16 Jun 2026 23:12:04 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c81e2aa56c38705c97ef031527a6f5a9205eb1113ca5e208985338f5c84f073`  
		Last Modified: Tue, 16 Jun 2026 23:12:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:9e3e322ee7d39da5cb6849240cd33b6721e7e2c4a49a2e91dca8234fddee679d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.5 KB (637500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7458c3893c0cfa3470be6ee24c7bf1b449a1030e18b0321abe23b155e1208d53`

```dockerfile
```

-	Layers:
	-	`sha256:cc2dddb6f2ddc5b9a284b0ecd56e780ccb07079ca9987eae592d64e6667221b8`  
		Last Modified: Tue, 16 Jun 2026 23:12:03 GMT  
		Size: 595.8 KB (595755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc3d57815eeb72d932507ff4b17ea0b85011ca9d4c47da9dbd4cff815731a2f4`  
		Last Modified: Tue, 16 Jun 2026 23:12:03 GMT  
		Size: 41.7 KB (41745 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.24` - linux; s390x

```console
$ docker pull postgres@sha256:4b2f739d1127986252bcf25d5612ae70500b263e8970858886c9be61d35f63ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123651427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65a5e250b2dcf428dc607300c518fcc57007138e9d70cba0c0235255273cf18`
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
ENV PG_MAJOR=17
# Tue, 16 Jun 2026 22:56:33 GMT
ENV PG_VERSION=17.10
# Tue, 16 Jun 2026 22:56:33 GMT
ENV PG_SHA256=078a03516dcdbdb705fecaf415ea3d13a956c589e46f09fed68a06fb00598c90
# Tue, 16 Jun 2026 22:56:33 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm21-dev 		clang21
# Tue, 16 Jun 2026 23:06:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm21/bin/llvm-config"; 	export CLANG=clang-21; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 16 Jun 2026 23:06:47 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 16 Jun 2026 23:06:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 16 Jun 2026 23:06:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 16 Jun 2026 23:06:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 16 Jun 2026 23:06:47 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 16 Jun 2026 23:06:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 16 Jun 2026 23:06:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 16 Jun 2026 23:06:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jun 2026 23:06:48 GMT
STOPSIGNAL SIGINT
# Tue, 16 Jun 2026 23:06:48 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 16 Jun 2026 23:06:48 GMT
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
	-	`sha256:3aee5f8096c2ab58b75971179de2f0042735f90c29a9b9e423e08d2389de35c4`  
		Last Modified: Tue, 16 Jun 2026 23:07:17 GMT  
		Size: 119.0 MB (119049995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0721bead5ac7e042b9d80aa80e8a4681dbd343d2c9b959c4b1a1d22f7825b6`  
		Last Modified: Tue, 16 Jun 2026 23:07:15 GMT  
		Size: 9.9 KB (9948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0a6426166a3f49dc050ee816a53ab28ccd08b7d9dfe071585ff5ee7e5d9ab5`  
		Last Modified: Tue, 16 Jun 2026 23:07:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112f93d83b9d1370dc44b640afe934b34a1c0f684130ce310e09fe328003c3d0`  
		Last Modified: Tue, 16 Jun 2026 23:07:15 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fb7027dc4023b0f293eeec78e6b32fe6fc89bef2f0151fe9e50aa7e748f29f`  
		Last Modified: Tue, 16 Jun 2026 23:07:15 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3150eabe86b18958341965e813407ab052b3b103d9e993332647f2d3e129be2b`  
		Last Modified: Tue, 16 Jun 2026 23:07:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.24` - unknown; unknown

```console
$ docker pull postgres@sha256:8d34d8ff24ee703302888cb820923ee416693cdafa3e9f242468c735abc199bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.1 KB (639069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fce7112ba0b7a9e22de079b4586bfeb26cb6f327e486dd0b7933fe9865f4e69`

```dockerfile
```

-	Layers:
	-	`sha256:ed871ccf9effad6b8fdb0bd062ba7c517d689ed71c83e8d6d6b1f2290754a991`  
		Last Modified: Tue, 16 Jun 2026 23:07:15 GMT  
		Size: 597.4 KB (597383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:693d988126f46fcffd811b063d4798843fa2ae7470734cc8e8f082db5f39d6a9`  
		Last Modified: Tue, 16 Jun 2026 23:07:15 GMT  
		Size: 41.7 KB (41686 bytes)  
		MIME: application/vnd.in-toto+json
