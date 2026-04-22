## `postgres:alpine3.22`

```console
$ docker pull postgres@sha256:af27ebd3413839ccfdcdf88e91ca76ad82117e52192067b76de9bb5be7ea6e04
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

### `postgres:alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:5af62d454ff2a5e88b2bcc9ec3a44b56267a8c6d5086a1e58135ee64230d4870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113422936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8293df341bf0d11cd9af7ae48832f607c3386243d3410f9e5ced4672341b9f86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:06:57 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:07:00 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:07:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:07:00 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:07:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:07:00 GMT
ENV PG_MAJOR=18
# Tue, 21 Apr 2026 23:07:00 GMT
ENV PG_VERSION=18.3
# Tue, 21 Apr 2026 23:07:00 GMT
ENV PG_SHA256=d95663fbbf3a80f81a9d98d895266bdcb74ba274bcc04ef6d76630a72dee016f
# Tue, 21 Apr 2026 23:07:00 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:09:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:09:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:09:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:09:17 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 21 Apr 2026 23:09:17 GMT
VOLUME [/var/lib/postgresql]
# Tue, 21 Apr 2026 23:09:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:09:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:09:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:09:17 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:09:17 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:09:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66dcea953279ea1d82469a254140388c60f62aba0f05b120052a8b67163f8cd`  
		Last Modified: Tue, 21 Apr 2026 23:09:32 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9cca1a729cca5e4be56d25a7a2d08493b3a0aadbcbb177a6925c89564e8c5b`  
		Last Modified: Tue, 21 Apr 2026 23:09:32 GMT  
		Size: 917.4 KB (917420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb689de9d2e83e7eaa5a8a4643e3efe3c7a9b4e038acffe0d5ee5f74451ec02`  
		Last Modified: Tue, 21 Apr 2026 23:09:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ef3d105d57748774a63dac08757266d12ba5a1e805d14d9a227b03131d79c3`  
		Last Modified: Tue, 21 Apr 2026 23:09:35 GMT  
		Size: 108.7 MB (108670911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737a26649bca8c6b2b7ac1831ad3b35bd3ac0a9380c28595e78d7b93a47b903d`  
		Last Modified: Tue, 21 Apr 2026 23:09:34 GMT  
		Size: 18.9 KB (18919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5906855a95ab931c658f52f40c1f743938db6390c9baa9dff317435756f65f`  
		Last Modified: Tue, 21 Apr 2026 23:09:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8024b1556bb5defccafcfbc2408bb70668d39cef0abfa0ebac40d6e0a7b7959`  
		Last Modified: Tue, 21 Apr 2026 23:09:34 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689579f23afa2453fffd82c656e3622e0ede8943387a91a68ec44316f08869cd`  
		Last Modified: Tue, 21 Apr 2026 23:09:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:fde13a3188250d5a3bdcd6e0f229139d58d38de324c155e5950cb2d4a302b1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.3 KB (655318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7a0afd2128e3c3f67283d71a802e5fc322ce149905d9e6556712c883add37f`

```dockerfile
```

-	Layers:
	-	`sha256:1c0fd8b95420e73c570bb157ca8233b49da7989ffcf1889b63fdc0d06c54da0e`  
		Last Modified: Tue, 21 Apr 2026 23:09:32 GMT  
		Size: 615.2 KB (615192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a84be13e5067734b514d4512741b53548be97215a7c496c8559a93b458aefa4`  
		Last Modified: Tue, 21 Apr 2026 23:09:33 GMT  
		Size: 40.1 KB (40126 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:28e792e835c6a751b14ab3eff79b27c8a5b4d9fb4fd4227fa3d10e4b94774297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92937712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7835c58b799079b1696da8d57dd0fcc07a54ec38eb1346f51d71e9aa8418ca24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:08:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:08:52 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:08:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:08:52 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:08:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:08:52 GMT
ENV PG_MAJOR=18
# Tue, 21 Apr 2026 23:08:52 GMT
ENV PG_VERSION=18.3
# Tue, 21 Apr 2026 23:08:52 GMT
ENV PG_SHA256=d95663fbbf3a80f81a9d98d895266bdcb74ba274bcc04ef6d76630a72dee016f
# Tue, 21 Apr 2026 23:08:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:11:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:11:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:11:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:11:46 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 21 Apr 2026 23:11:46 GMT
VOLUME [/var/lib/postgresql]
# Tue, 21 Apr 2026 23:11:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:11:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:11:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:11:46 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:11:46 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:11:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c537698d2fde0e69700563990859aa1b702da3921cef6bbba6c51618e56c7d`  
		Last Modified: Tue, 21 Apr 2026 23:11:57 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81acbeab268d11e2212642674da74ee162d09b7ce29c67a96a946f6bae197754`  
		Last Modified: Tue, 21 Apr 2026 23:11:57 GMT  
		Size: 885.2 KB (885152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c74f28535b59ab664554a83fb187f5ccc2d55ea911ed187c2db0e3376934cc`  
		Last Modified: Tue, 21 Apr 2026 23:11:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c52f151fa39d591018ca60ac7f731b7b248d97c24c00c25a3f8c5df1e593aab`  
		Last Modified: Tue, 21 Apr 2026 23:12:00 GMT  
		Size: 88.5 MB (88518770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331c9633dd198c7a0e5c3e78b399a2f13576bb6cb3c6c5a0399db10f91e85472`  
		Last Modified: Tue, 21 Apr 2026 23:11:58 GMT  
		Size: 18.9 KB (18916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9393183ef0ef3fcb7de890cac2e425ed2f7e98b71bdaf71c49a115cfe4d38955`  
		Last Modified: Tue, 21 Apr 2026 23:11:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a3754e91e4c62be6df321e7124b716d86bc707090d9f21d29f737fb2d8144a`  
		Last Modified: Tue, 21 Apr 2026 23:11:58 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2819bf16529da6177512375cd150a83590859e34b154e1a18595aa0b4c4b04`  
		Last Modified: Tue, 21 Apr 2026 23:11:59 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:5b7197bd64b6fd5c44809c682e6b67ac81ce01e54db315f20f0f9c0293b255b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f252696bc9fd5fa7ea78a6517bfad5e0e89dc147c439323c757f0fc61d4417`

```dockerfile
```

-	Layers:
	-	`sha256:672fefbe19ad1e3645260769ecb95ca6ff20343e2516b88c932022408763f58f`  
		Last Modified: Tue, 21 Apr 2026 23:11:57 GMT  
		Size: 40.1 KB (40056 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:3381b8590dd64d00f1995a8820da173c68d4e33c05d868e976117d09056f3394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88048289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3adea14f5434846edff9ef8b3106d49176623f3c9b34bf58ec6df2bcaf65d93b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:28:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:28:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:28:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:28:48 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:28:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:28:48 GMT
ENV PG_MAJOR=18
# Tue, 21 Apr 2026 23:28:48 GMT
ENV PG_VERSION=18.3
# Tue, 21 Apr 2026 23:28:48 GMT
ENV PG_SHA256=d95663fbbf3a80f81a9d98d895266bdcb74ba274bcc04ef6d76630a72dee016f
# Tue, 21 Apr 2026 23:28:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:31:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:31:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:31:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:31:38 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 21 Apr 2026 23:31:38 GMT
VOLUME [/var/lib/postgresql]
# Tue, 21 Apr 2026 23:31:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:31:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:31:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:31:38 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:31:38 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:31:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc99c4d00d38c7b1a614b4d47e0dfdc61cd7612c3746cc8aa8d2595416ae2a59`  
		Last Modified: Tue, 21 Apr 2026 23:31:49 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d424a56459fecb40b1ab895baf729af9e6e51e0e62f8bba65fbfe9c8a47a1b`  
		Last Modified: Tue, 21 Apr 2026 23:31:50 GMT  
		Size: 885.2 KB (885151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2db38ad8f9335387ffadd4ba71792d4e56ee48261ff26fe5f5e776c07b95a03`  
		Last Modified: Tue, 21 Apr 2026 23:31:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14b79787f265879091a88bc8d2611e0e9bbe70929ca6c367adb91baacf93d04`  
		Last Modified: Tue, 21 Apr 2026 23:31:52 GMT  
		Size: 83.9 MB (83910892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219a342700af4429f5f692a304e231342a2cac2af9087f88a6a3a7a3c80d7e06`  
		Last Modified: Tue, 21 Apr 2026 23:31:51 GMT  
		Size: 18.9 KB (18919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3bcb933eb04026926e3c0fb7d4c4e000183b6571af4f5b5432405165d55c62`  
		Last Modified: Tue, 21 Apr 2026 23:31:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa1211f03ef89b13101331ad8ff5ced9383daffea0f41c0c4ea788af198e31b`  
		Last Modified: Tue, 21 Apr 2026 23:31:51 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ec220aecf4334de5cfde08f911a463ebdd1e3014ea5c07b72fe51e34deda17`  
		Last Modified: Tue, 21 Apr 2026 23:31:52 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:7b34d2ccac1137f255646c081da3250d4d042c1f51a59883ccddba90e1e38e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.5 KB (655491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9da021d3c5f9b350847dd70cf00535060d9115d87660fdc001c72c54054a36e`

```dockerfile
```

-	Layers:
	-	`sha256:76b19c3725e7e9ca1566ef8baf045f2370e72a6c6a5ec866528537842857b2d2`  
		Last Modified: Tue, 21 Apr 2026 23:31:50 GMT  
		Size: 615.2 KB (615220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f981e9a0073d3e976a15e1f315f9bb78965524af698eb0500e58dbdc1c21af8c`  
		Last Modified: Tue, 21 Apr 2026 23:31:49 GMT  
		Size: 40.3 KB (40271 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:97adc764004368fb1a0c2d6f33cc6738cfbce1a8ed160c8b89283b8aaa72ba31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109408871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361669f3f5a4a24cf79ea5247a80915e4953a1bd057c048910e57e187d84445a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:08:07 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:08:09 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:08:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:08:09 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:08:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:08:09 GMT
ENV PG_MAJOR=18
# Tue, 21 Apr 2026 23:08:09 GMT
ENV PG_VERSION=18.3
# Tue, 21 Apr 2026 23:08:09 GMT
ENV PG_SHA256=d95663fbbf3a80f81a9d98d895266bdcb74ba274bcc04ef6d76630a72dee016f
# Tue, 21 Apr 2026 23:08:09 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:10:42 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:10:42 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:10:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:10:42 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 21 Apr 2026 23:10:42 GMT
VOLUME [/var/lib/postgresql]
# Tue, 21 Apr 2026 23:10:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:10:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:10:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:10:42 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:10:42 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:10:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3bde812751c4cbb7066e07c114361e6e536dd07dd587ce75383e6b587ae10d`  
		Last Modified: Tue, 21 Apr 2026 23:10:58 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee92fb1723cc4470de08167919ba9b2b3b20a2c213035ddb0346961a661ba6d`  
		Last Modified: Tue, 21 Apr 2026 23:10:58 GMT  
		Size: 873.1 KB (873130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e2fe0f530fbdaaf6108bec12695720f07526426722c99bd754117c447dad70`  
		Last Modified: Tue, 21 Apr 2026 23:10:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a046cc24bcec66a9cf7522a9c2e1d825151eb6c4b1883f75c84e9d6e7ff744eb`  
		Last Modified: Tue, 21 Apr 2026 23:11:02 GMT  
		Size: 104.4 MB (104367428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18013b8e41b44997ca398fd0f30b56decb57ba8266987b28673a75c55856df`  
		Last Modified: Tue, 21 Apr 2026 23:10:59 GMT  
		Size: 18.9 KB (18919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a083ac851457d223e6fa61d38ec0d6058ca05cdc0c0f8dc5377dd57569cf6dd6`  
		Last Modified: Tue, 21 Apr 2026 23:11:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91559f9b84b9cee2a125930212eca2fae382d9287c979523d615e1bf71afb003`  
		Last Modified: Tue, 21 Apr 2026 23:11:00 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbd7a22ba501ffe32440afca833ab25526d5c1409d19711ce1419d0f9b08e51`  
		Last Modified: Tue, 21 Apr 2026 23:11:01 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:949ba633ddc04a605a080b390916be9bb6fbd3539a3b1f406879ab08f8395450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.5 KB (655544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0968921b7c53e69150f430ebb3761a7710c10fc0e4d99be8953a5f9d44f71855`

```dockerfile
```

-	Layers:
	-	`sha256:7bb62ebff33d69740a5ecb070ff10331ff251050233efade7a8b80d2d048150c`  
		Last Modified: Tue, 21 Apr 2026 23:10:58 GMT  
		Size: 615.2 KB (615236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:062c4e5cd2b910f555412104572249deaa33a932c0abb8c350cac526da5160fb`  
		Last Modified: Tue, 21 Apr 2026 23:10:58 GMT  
		Size: 40.3 KB (40308 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:a6c5bd4850349dc1cb70835c2b1dfbe88a9150cc6b06824d40d21079623a231f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119833024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b130d4a66cac46653ede486d3df437b70648b4b6ef74abe7ad62e4b177032f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:08:52 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:08:56 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:08:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:08:56 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:08:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:08:56 GMT
ENV PG_MAJOR=18
# Tue, 21 Apr 2026 23:08:56 GMT
ENV PG_VERSION=18.3
# Tue, 21 Apr 2026 23:08:56 GMT
ENV PG_SHA256=d95663fbbf3a80f81a9d98d895266bdcb74ba274bcc04ef6d76630a72dee016f
# Tue, 21 Apr 2026 23:08:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:11:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:11:45 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:11:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:11:45 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 21 Apr 2026 23:11:45 GMT
VOLUME [/var/lib/postgresql]
# Tue, 21 Apr 2026 23:11:45 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:11:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:11:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:11:45 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:11:45 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:11:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0cf91f4f45192f4ad675d9a4c8f8fb0f9734f57af2a920de6369b84d74a32e`  
		Last Modified: Tue, 21 Apr 2026 23:12:00 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f736a73d2e22900f84f334731fdaa0253cc6384086983bb414a42117bcdbe1b9`  
		Last Modified: Tue, 21 Apr 2026 23:12:01 GMT  
		Size: 889.8 KB (889753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67596777803d729d5fd4f15462b10c30cedb540896f72647c9a8433fc961568b`  
		Last Modified: Tue, 21 Apr 2026 23:12:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b5be312da053fe5204aa603d0026a9d54eeb8a63960e25630c3a203dc4bd1a`  
		Last Modified: Tue, 21 Apr 2026 23:12:04 GMT  
		Size: 115.3 MB (115292133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d6ab42aa83fd287ab62a9f3a81c6d57bdeae4bf6dfbbea4203fe4c59833e3`  
		Last Modified: Tue, 21 Apr 2026 23:12:02 GMT  
		Size: 18.9 KB (18920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8340bf695e5a7bd36a051fde69fed2e97abfb9561bd7d1f4eaee7780fa578f`  
		Last Modified: Tue, 21 Apr 2026 23:12:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79e5d8fc780747db5b2b9db3ff52996cd5c1d045c6e1b8accd486dbce779c26`  
		Last Modified: Tue, 21 Apr 2026 23:12:02 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fd9d9bf660b0a03136cd78bdc504e8543916669f0c4ce78ecb9ef56c50e454`  
		Last Modified: Tue, 21 Apr 2026 23:12:03 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:5c85164d39249104f5354754bd616097975a2b454ab0b037aef7f1745c49d63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.3 KB (655259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339d310ddc3d30a7fe1ca9159a8c26c8f488a6d313b56180578c3f79f9afadae`

```dockerfile
```

-	Layers:
	-	`sha256:e86b74865ea135ee56453bb862c77a22ec0c7a264f79378c3a016b7f506cc4c5`  
		Last Modified: Tue, 21 Apr 2026 23:12:01 GMT  
		Size: 615.2 KB (615172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98b5ffd42bdd6d82d651a8f1ae4d9821aec38485415c373641b25e48d99fc11f`  
		Last Modified: Tue, 21 Apr 2026 23:12:01 GMT  
		Size: 40.1 KB (40087 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:57365cd339a399c9942a3d22402edffaa6ca834a2fd496eebcd26ef3b6527c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97441463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a5efde82b7ea507e4b18fe11902232eba9915128861d0d9aaed1e2f71c1b90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:55:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 17 Apr 2026 00:56:01 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Apr 2026 00:56:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 00:56:01 GMT
ENV LANG=en_US.utf8
# Fri, 17 Apr 2026 00:56:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 00:56:01 GMT
ENV PG_MAJOR=18
# Fri, 17 Apr 2026 00:56:01 GMT
ENV PG_VERSION=18.3
# Fri, 17 Apr 2026 00:56:01 GMT
ENV PG_SHA256=d95663fbbf3a80f81a9d98d895266bdcb74ba274bcc04ef6d76630a72dee016f
# Fri, 17 Apr 2026 00:56:01 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 17 Apr 2026 01:00:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 17 Apr 2026 01:00:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 17 Apr 2026 01:00:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 17 Apr 2026 01:00:21 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 17 Apr 2026 01:00:21 GMT
VOLUME [/var/lib/postgresql]
# Tue, 21 Apr 2026 23:43:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:43:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:43:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:43:25 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:43:25 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:43:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994fd3b166293e4617ca5472a952e8dc21082efd9682a43943df39ebcf544ae4`  
		Last Modified: Fri, 17 Apr 2026 01:01:06 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2b60bc8e7f425f63f0830c9466a974ba3e426f197d170fb82acc065521ab50`  
		Last Modified: Fri, 17 Apr 2026 01:01:06 GMT  
		Size: 878.3 KB (878310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e352e777c9beceff0496bb0d290e171684587a097a3b2f1bba1c67b4c3e3b13f`  
		Last Modified: Fri, 17 Apr 2026 01:01:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485608968abe6bc89f5e4d303ea8e44b54632f541e0e0e2bd30e510ef7b3c827`  
		Last Modified: Fri, 17 Apr 2026 01:01:10 GMT  
		Size: 92.8 MB (92800072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2edc49b70cc771a514d168ec4c1474e6400fa497ff7036553c5a09ba070db1c`  
		Last Modified: Fri, 17 Apr 2026 01:01:08 GMT  
		Size: 18.9 KB (18919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a8a29eac0348e90761a0a34475618e08894f2fcb438082faf05fd658b0868e`  
		Last Modified: Fri, 17 Apr 2026 01:01:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3e5a0507331d09f86ee3bd1ad5393cd89301539988284964cbb00db861ff90`  
		Last Modified: Tue, 21 Apr 2026 23:43:43 GMT  
		Size: 6.1 KB (6102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f179a24d9cc876a3f2f70262fb75c82fd8f3075ab1a4089e3383bf65864a9e7`  
		Last Modified: Tue, 21 Apr 2026 23:43:43 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:30f05655413b9a686a246632719a9a2c762ec7730b075ebb4a933d11d9106553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.8 KB (651778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d41556b942e13955d11eeefbcb50dae0b825042d410070a668b549789e93b9`

```dockerfile
```

-	Layers:
	-	`sha256:997e1827957953981453307af5bd914f01635aa4c32a8bab556a442329079241`  
		Last Modified: Tue, 21 Apr 2026 23:43:43 GMT  
		Size: 611.6 KB (611607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77e76a732fde131670ca0875ade8521ff435bcf850b6324dcb268630a5f88dc7`  
		Last Modified: Tue, 21 Apr 2026 23:43:43 GMT  
		Size: 40.2 KB (40171 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:157c846ce02a218ccbbec5452864707d3d2d29bc1f4b3419173a23e2daffc90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.7 MB (113695103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5dbca4e8b2905c45254f298097debe33352ec3c7c84a9cf3197537cadf87d6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Apr 2026 22:19:29 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 18 Apr 2026 22:19:41 GMT
ENV GOSU_VERSION=1.19
# Sat, 18 Apr 2026 22:19:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 18 Apr 2026 22:19:41 GMT
ENV LANG=en_US.utf8
# Sat, 18 Apr 2026 22:19:42 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 18 Apr 2026 22:19:42 GMT
ENV PG_MAJOR=18
# Sat, 18 Apr 2026 22:19:42 GMT
ENV PG_VERSION=18.3
# Sat, 18 Apr 2026 22:19:42 GMT
ENV PG_SHA256=d95663fbbf3a80f81a9d98d895266bdcb74ba274bcc04ef6d76630a72dee016f
# Sat, 18 Apr 2026 22:19:42 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 18 Apr 2026 23:09:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 18 Apr 2026 23:09:29 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 Apr 2026 02:36:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 22 Apr 2026 02:36:36 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 22 Apr 2026 02:36:36 GMT
VOLUME [/var/lib/postgresql]
# Wed, 22 Apr 2026 02:36:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:36:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 02:36:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:36:36 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 02:36:36 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 02:36:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587d8e2fd99fe429bf8f22467e93aa876a5641cf7de4fb04ba99bc68a0de695d`  
		Last Modified: Sat, 18 Apr 2026 23:12:22 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a506d334faeab2227b02d175475320187eefeaba57ea193e2009ba29e541869c`  
		Last Modified: Sat, 18 Apr 2026 23:12:22 GMT  
		Size: 865.7 KB (865729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096e923fa3664133bf08c68edc7653025b0c8faa5cc2f2a2525e7e47b2c487dd`  
		Last Modified: Sat, 18 Apr 2026 23:12:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6179364ac90b812649935ecd9f059860f897b45ccc3c109b8160ec0643cdcb0e`  
		Last Modified: Sat, 18 Apr 2026 23:12:38 GMT  
		Size: 109.3 MB (109282062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0ce16ea49f0cdd40778b0ca10583b14c1e6b248fa440670007175d25a89c3e`  
		Last Modified: Sat, 18 Apr 2026 23:12:23 GMT  
		Size: 18.9 KB (18928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691a02e55229d593763621555aabc3a8cf310f40f39cf9076507ffdfe2f1975f`  
		Last Modified: Wed, 22 Apr 2026 02:37:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15606236a68b0116ae967134048ae25dd73c54da06582228c66c4ff45a18936a`  
		Last Modified: Wed, 22 Apr 2026 02:37:52 GMT  
		Size: 6.1 KB (6102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f1227e6b6be958b29cc116f78e83c0a83810cc37b302689ed30f941eed30f1`  
		Last Modified: Wed, 22 Apr 2026 02:37:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:5afdb7c6124b2a3e22fa67c54b68adb3492082cd27c17dcbd79cd0c86263810e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.4 KB (653441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5697134441b483f41c2ade87607aa8981b05776a6041c9287f730bda0124514d`

```dockerfile
```

-	Layers:
	-	`sha256:ca04332f97147e9f7de535b37cf4b93e0235198025119d5a044b8fc67a9e5d59`  
		Last Modified: Wed, 22 Apr 2026 02:37:52 GMT  
		Size: 613.3 KB (613265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d78baae3c039dea03197450bcb401c123a86713f758eeb6ebd0e12cdf51697f`  
		Last Modified: Wed, 22 Apr 2026 02:37:52 GMT  
		Size: 40.2 KB (40176 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:d90e502c5ec79615558426f1fd456ab90697b5ab8ac8def67b12f72602225425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122316678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e48371934fd80a05fe978a2a8ec02fffcfd7da91e1283a0be5ba6268e41f00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:03 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 17 Apr 2026 00:32:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Apr 2026 00:32:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 00:32:07 GMT
ENV LANG=en_US.utf8
# Fri, 17 Apr 2026 00:32:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 00:32:07 GMT
ENV PG_MAJOR=18
# Fri, 17 Apr 2026 00:32:07 GMT
ENV PG_VERSION=18.3
# Fri, 17 Apr 2026 00:32:07 GMT
ENV PG_SHA256=d95663fbbf3a80f81a9d98d895266bdcb74ba274bcc04ef6d76630a72dee016f
# Fri, 17 Apr 2026 00:32:07 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 17 Apr 2026 00:36:38 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 17 Apr 2026 00:36:39 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 17 Apr 2026 00:36:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 17 Apr 2026 00:36:39 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 17 Apr 2026 00:36:39 GMT
VOLUME [/var/lib/postgresql]
# Tue, 21 Apr 2026 23:05:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:05:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:05:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:05:56 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:05:56 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:05:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b16b5e74609982c1b9aa44c4a27109093c4a3ba6b88e0e3fc5d1210eed2a213`  
		Last Modified: Fri, 17 Apr 2026 00:37:05 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1b45c8d73f888134c6fdd2bcde4cf95a1878d8360dcd10f1aa2c3e7fdead26`  
		Last Modified: Fri, 17 Apr 2026 00:37:05 GMT  
		Size: 894.2 KB (894238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320b21e60320ebeb63441338623b5d5915316e75a3824a868dfca204896c432f`  
		Last Modified: Fri, 17 Apr 2026 00:37:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19126c1c33451494d8f48101f6f97c5689efadaea664d92640c95e863bf0236b`  
		Last Modified: Fri, 17 Apr 2026 00:37:08 GMT  
		Size: 117.7 MB (117742147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7dfd2b13e421b44605a082ce5b2849ac5f916dd1822617197596acb545b2dba`  
		Last Modified: Fri, 17 Apr 2026 00:37:06 GMT  
		Size: 18.9 KB (18920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d23bc347cc23a8d2fccf6c45989b00a61766e924654e4b1daac9702b5ceecf`  
		Last Modified: Fri, 17 Apr 2026 00:37:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0b21218b6fd21c36fd7aff4355514a45df777b7d7ce7c701bf39526e20c37`  
		Last Modified: Tue, 21 Apr 2026 23:06:10 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d630c658c20224f035c1c8b5d974011bc38292097854685124c475126ace8ee`  
		Last Modified: Tue, 21 Apr 2026 23:06:10 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:3461901d24565f32eb19d273389f24107ba35c23c1433decaac2e399580d8e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.4 KB (653367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c784df95892d8b2dbb0fb1a7b8b5374c86752b039bd503a7ba0f9c360c234c5`

```dockerfile
```

-	Layers:
	-	`sha256:02ecf31f6e768dd1ba8b60e740c16e81e4ff3e896b0099c1f3aa5e153fead64c`  
		Last Modified: Tue, 21 Apr 2026 23:06:10 GMT  
		Size: 613.2 KB (613241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c61359e5cb17455d3dfb3619cd17261d8464b8b35cdca295ba811e0471e21ac`  
		Last Modified: Tue, 21 Apr 2026 23:06:10 GMT  
		Size: 40.1 KB (40126 bytes)  
		MIME: application/vnd.in-toto+json
