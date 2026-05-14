## `postgres:18-alpine3.22`

```console
$ docker pull postgres@sha256:3043d6e864e9164252afd5e60c9412c2d6c3da02a33cb6ba3e7f03d005d0cb50
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

### `postgres:18-alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:56ba71bf54060de15a6b2df1a18081b8f6c5bf61255b7ed6f1ef10ee868eaff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.5 MB (113490912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646c746f3bfbad9bba5cd22c10a43e0cf5b219adfadab09fabc6432a9e961bc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 19:01:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 19:01:15 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 19:01:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:01:15 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:01:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:01:15 GMT
ENV PG_MAJOR=18
# Thu, 14 May 2026 19:01:15 GMT
ENV PG_VERSION=18.4
# Thu, 14 May 2026 19:01:15 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Thu, 14 May 2026 19:01:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:03:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:03:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:03:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:03:23 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 May 2026 19:03:23 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 May 2026 19:03:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:03:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:03:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:03:23 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:03:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:03:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691684e6aaf1fe1f554270ab596fa59e3eb7bf28b61574dc40db193296fe35e8`  
		Last Modified: Thu, 14 May 2026 19:03:38 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276638d392be210527611c9d260799a6b19bfa5fd0e248b212e8885520745b24`  
		Last Modified: Thu, 14 May 2026 19:03:38 GMT  
		Size: 917.4 KB (917416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01898b0f2f8f4145a951b351a4740ed447204f469f6eed2ad782126b07522acb`  
		Last Modified: Thu, 14 May 2026 19:03:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2b19547695c7580045082ef2a87c95318bf1789c6c8b651058da36c7a5adcd`  
		Last Modified: Thu, 14 May 2026 19:03:40 GMT  
		Size: 108.7 MB (108738884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0824ba9d99748fb8c0d457623671db6d57cc0e01bf2f57f3307ec5c6cb4f4344`  
		Last Modified: Thu, 14 May 2026 19:03:39 GMT  
		Size: 18.9 KB (18921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b985519e9efe04cbd383d826b014897fa55da99e1d66a59195913f74f8622d`  
		Last Modified: Thu, 14 May 2026 19:03:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7966da69b44e5f5182e0e3e55ccd94567d5b4af5d96af3334dab1768f10a2e43`  
		Last Modified: Thu, 14 May 2026 19:03:39 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b595b2a32ef05ccd422cfd6789cd865e5b1c0090113f0cc5c0dfe0d5ea3a50`  
		Last Modified: Thu, 14 May 2026 19:03:40 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:59dad03329ad56d3e7c8ab1f8feedb63d5da8c01ba26f05ccb909f62f7d35ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.3 KB (655318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf881b01ebcf21b65891001f9ae4ae911dcbf0ec6d4a6574280fcf07d96716c`

```dockerfile
```

-	Layers:
	-	`sha256:990d48ff9ee25cd36ce3fdbb7105b7dfa480b48453121f986165705a38b3f84f`  
		Last Modified: Thu, 14 May 2026 19:03:38 GMT  
		Size: 615.2 KB (615192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d16a5df396c2594595ece006b36737aafc1489be1a9f738c8ead7c5d51d645e4`  
		Last Modified: Thu, 14 May 2026 19:03:38 GMT  
		Size: 40.1 KB (40126 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:c048b846abcb8a6ce35781f99e7da8ff63cc99e1102eb2372d9316f782f213c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93003128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4bad946ca379547e017e09e8d413ea3248cc3a61199c1057d858c89156c58d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 19:13:04 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 19:13:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 19:13:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:13:08 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:13:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:13:08 GMT
ENV PG_MAJOR=18
# Thu, 14 May 2026 19:13:08 GMT
ENV PG_VERSION=18.4
# Thu, 14 May 2026 19:13:08 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Thu, 14 May 2026 19:13:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:16:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:16:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:16:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:16:13 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 May 2026 19:16:13 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 May 2026 19:16:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:16:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:16:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:16:13 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:16:13 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:16:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3876bf8c8409b05a8b53dba04a191853647473c833511cdfa2ccbae4db9dd68e`  
		Last Modified: Thu, 14 May 2026 19:16:25 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1262241bcc7a62d4db021bbb3b3551dc01e4a1a3e074e84715205e3e83ba66`  
		Last Modified: Thu, 14 May 2026 19:16:25 GMT  
		Size: 885.1 KB (885150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71619fa1b03e91a29c935bda915540099177442f8f546acc22001d0b84ffb68e`  
		Last Modified: Thu, 14 May 2026 19:16:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1100fee19b9c65ebfc4df6cf60f585a876b6d6e16337a3f567c5b63a316cb5d`  
		Last Modified: Thu, 14 May 2026 19:16:27 GMT  
		Size: 88.6 MB (88584187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3c7bce54d31c49d289e0a9567b32a2eb8eef5017fc1afb8f3be97cc35d485b`  
		Last Modified: Thu, 14 May 2026 19:16:26 GMT  
		Size: 18.9 KB (18917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bed77ee0c27d4472c02dfc427244e5285f508869e5ebc6d218c9b37c712ccb`  
		Last Modified: Thu, 14 May 2026 19:16:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd893af5b33178e9118f60d85c4eb08be783772f53cccdf43650aa5128fb9437`  
		Last Modified: Thu, 14 May 2026 19:16:27 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c978802267c99c57d8c0a28c308e24c8f46815c15f886555563eefcc3d477703`  
		Last Modified: Thu, 14 May 2026 19:16:27 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:3fb3bf6483252330584428a08004286a6c8579d3dde25c0978a18d71b9a2cff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 KB (40056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d20b00136bc4f3402bd80fc64e106404cc9c79412b19dfe22c863bf9b2c6eb`

```dockerfile
```

-	Layers:
	-	`sha256:2238ec89bea2fcabac452c800f214d92f0c373bd716a40ad976287b610555cf5`  
		Last Modified: Thu, 14 May 2026 19:16:25 GMT  
		Size: 40.1 KB (40056 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b0741d220cdfdc44721399381b4d33ed1508843e79d5c9cda9a18489af4f9a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88106990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556854efe6faa902a1d893ecfc19d8027968343494212cb3412049fb0348bb08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 18:57:58 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 18:58:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 18:58:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 18:58:01 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 18:58:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 18:58:01 GMT
ENV PG_MAJOR=18
# Thu, 14 May 2026 18:58:01 GMT
ENV PG_VERSION=18.4
# Thu, 14 May 2026 18:58:01 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Thu, 14 May 2026 18:58:01 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:00:53 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:00:53 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:00:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:00:53 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 May 2026 19:00:53 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 May 2026 19:00:53 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:00:53 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:00:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:00:53 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:00:53 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:00:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc698dd811c41710c02400b64ab517cccecbd6d507ad6794e8442795378dbed`  
		Last Modified: Thu, 14 May 2026 19:01:05 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984982d080265d7b96585a8f21fcd9afb133db20c78bff35a61b22f8012777a1`  
		Last Modified: Thu, 14 May 2026 19:01:05 GMT  
		Size: 885.2 KB (885152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09dad5f39df8a4193848d52cfe6d9518a74778f468c9bfc72ca1c17c51049a30`  
		Last Modified: Thu, 14 May 2026 19:00:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c24d545f119b95ed5893a5f5075341f0c3a32d36ce66dda37765eaff061132`  
		Last Modified: Thu, 14 May 2026 19:01:11 GMT  
		Size: 84.0 MB (83969601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5df2fc35684abb0d3e338ff47e1dce8b0a31c4897c47c32727c0e74acab1fe6`  
		Last Modified: Thu, 14 May 2026 19:01:09 GMT  
		Size: 18.9 KB (18917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce68ee9188d2ba4a69fe0b50a5d8436510865e78f2b8c44bcdbf315da38fd76`  
		Last Modified: Thu, 14 May 2026 19:01:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366a5e30ec9c03b315ac635f8fc32e69ab30c151bd4accd927b936b903990a26`  
		Last Modified: Thu, 14 May 2026 19:01:07 GMT  
		Size: 6.1 KB (6092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec5f1d65ad7f52eed6b20c5619a985f8f8cd4c4063ed51a3dbd6545c33b4cee`  
		Last Modified: Thu, 14 May 2026 19:01:10 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:8caf53aee9b0c2d03d72ec6d7aa0f223a3d0383e918f282a985fdc5610d6a611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.5 KB (655491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4164f982508077970a6990892f321cbd205c0a111e3e47945b463ae35d41419c`

```dockerfile
```

-	Layers:
	-	`sha256:3372838d3f63d4b4a8ea7cd4277eaf63756e4e9e2a1775577952d29f11b5e975`  
		Last Modified: Thu, 14 May 2026 19:01:06 GMT  
		Size: 615.2 KB (615220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:169843894c3117486890eef34f93c028d3ea0da77a3343257f566baf3e276ec5`  
		Last Modified: Thu, 14 May 2026 19:01:07 GMT  
		Size: 40.3 KB (40271 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:d8f58196f91e267e1864783179a145f2f9cfb8ecbb76bc56b6d33acd0c9de2da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109458539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228eb4db8091282017abc92b3d20c2b31b843eea7d489e9af6e68678c9117372`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 18:57:58 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 18:58:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 18:58:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 18:58:01 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 18:58:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 18:58:01 GMT
ENV PG_MAJOR=18
# Thu, 14 May 2026 18:58:01 GMT
ENV PG_VERSION=18.4
# Thu, 14 May 2026 18:58:01 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Thu, 14 May 2026 18:58:01 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:00:27 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:00:28 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:00:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:00:28 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 May 2026 19:00:28 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 May 2026 19:00:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:00:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:00:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:00:28 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:00:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:00:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e835a21db7c804372d76cc7bd18eb7c7e1da93de2ae674552422db39804413fe`  
		Last Modified: Thu, 14 May 2026 19:00:44 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5b2c7d010e711821f55f183c8c2cb6a66f060b126f657abef4f49a7b0df00d`  
		Last Modified: Thu, 14 May 2026 19:00:44 GMT  
		Size: 873.1 KB (873132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09dad5f39df8a4193848d52cfe6d9518a74778f468c9bfc72ca1c17c51049a30`  
		Last Modified: Thu, 14 May 2026 19:00:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3703b4810c045a92d71bdcbb2eb7424b1cc08a59134e3e4f10e7b5afbd13ed03`  
		Last Modified: Thu, 14 May 2026 19:00:47 GMT  
		Size: 104.4 MB (104417096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bd1ab9aca7fb191d2639ddb2b720eec66263456a44894fd1c9afe6927d71db`  
		Last Modified: Thu, 14 May 2026 19:00:46 GMT  
		Size: 18.9 KB (18921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64e81ea16280400b7c836189f091f3b93e43b2160001bda57a6189a027350ff`  
		Last Modified: Thu, 14 May 2026 19:00:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a622c3f7e7b7a2990edfe4ed57d75a4f41f4d59ff12fb036a8515d8c42fac1`  
		Last Modified: Thu, 14 May 2026 19:00:46 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da9791ba5955b406b3ff172d0a8a398cbb720cc4e2357ec917cd5b355065045`  
		Last Modified: Thu, 14 May 2026 19:00:47 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:c90f6b731edfde8994ea1e91fbf6065162fb14b3e457cec7d74abb9dbf11f67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.5 KB (655544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759dd11d8b6eb01929e713cedeb3b7ee22b4ec59246bd488f6573bd234911966`

```dockerfile
```

-	Layers:
	-	`sha256:e78b6b113e8dd98efdcb4f39bc0275f4a88667550fda32affb4920c50e9eb59d`  
		Last Modified: Thu, 14 May 2026 19:00:44 GMT  
		Size: 615.2 KB (615236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a22ad571e2725ab4f663b0d477cac2cad39243504c170a35398634e48364128`  
		Last Modified: Thu, 14 May 2026 19:00:45 GMT  
		Size: 40.3 KB (40308 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:1373a8b4d3702b7b3cf856bea94987fe52b379803d9d5b34b708439c764762a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119896258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9900beba83a2d78965470c96f6651845a00dfb9fc026c8a7495b844971e2fade`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 18:58:31 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 18:58:37 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 18:58:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 18:58:37 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 18:58:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 18:58:37 GMT
ENV PG_MAJOR=18
# Thu, 14 May 2026 18:58:37 GMT
ENV PG_VERSION=18.4
# Thu, 14 May 2026 18:58:37 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Thu, 14 May 2026 18:58:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:01:35 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:01:36 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:01:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:01:36 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 May 2026 19:01:36 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 May 2026 19:01:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:01:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:01:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:01:36 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:01:36 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:01:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadf06fd1d7c48a29dfe032ce547ff71ee7378a811647be9ab69c88e1ff0a175`  
		Last Modified: Thu, 14 May 2026 19:01:55 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e50e354813035b6f1ed38320da9bcda56426d9677d012bf8f4828075c934a1`  
		Last Modified: Thu, 14 May 2026 19:01:55 GMT  
		Size: 889.7 KB (889748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a93ead2f877a90b54ec29fbcdd6422dfc374b3f1f1ed896fcef6aa0e439bf37`  
		Last Modified: Thu, 14 May 2026 19:01:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5efdd404995e81a964026bf3d0ded53a07841120eef9fdf5f91ce1df90fab0`  
		Last Modified: Thu, 14 May 2026 19:01:58 GMT  
		Size: 115.4 MB (115355367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ac5402f18565b3aa9c0a18dc620dad7c5c2fade3b02c9693a7c360688dc184`  
		Last Modified: Thu, 14 May 2026 19:01:56 GMT  
		Size: 18.9 KB (18922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562eee89d6bb2d05e9fe26799e4d07980a55cf26e450d2572bfb9b3d3ce4ae3c`  
		Last Modified: Thu, 14 May 2026 19:01:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8386556c8f60066a8adc78b0fd82e4293c814469bd143bf1a745d3e199331d`  
		Last Modified: Thu, 14 May 2026 19:01:57 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81758e0f2dafae8abb205f0ff551df3be39a1f3964a2663cc0b6a700a6e7358`  
		Last Modified: Thu, 14 May 2026 19:01:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:3b813b65ea773fd9305ed986155dabaa6816c27878dfd78109e43b20c1e13ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.3 KB (655259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be8fb23978c37c3d69cc2387df362e1a256f1ae14701fd4f5b5c96150398af7`

```dockerfile
```

-	Layers:
	-	`sha256:85ab9afdf9dcf98d27fbd20e55a1f2ab21835df0e6e965480c8f98bc8f7f7fd2`  
		Last Modified: Thu, 14 May 2026 19:01:55 GMT  
		Size: 615.2 KB (615172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dca11bde5d5e0756c68248d127cc998c57a676ff76decc8ff738bb2d6efd10c3`  
		Last Modified: Thu, 14 May 2026 19:01:55 GMT  
		Size: 40.1 KB (40087 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:3b6f7049d85c87248985a6fc1cb20febd557fcde02fe262d60b63f7a54284de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97501942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faeb92f23304ab4b8ee396798cbba65a50fed4b09ddd69b8ebc79f1dcda9b6fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 19:32:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 19:32:48 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 19:32:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:32:48 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:32:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:32:48 GMT
ENV PG_MAJOR=18
# Thu, 14 May 2026 19:32:48 GMT
ENV PG_VERSION=18.4
# Thu, 14 May 2026 19:32:48 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Thu, 14 May 2026 19:32:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 19:36:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 19:36:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:36:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:36:09 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 May 2026 19:36:09 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 May 2026 19:36:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:36:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:36:10 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:36:10 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:36:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063a9d5349dd7c559d9d4da649111e6f9ab000e140d7cddeb891987f33961190`  
		Last Modified: Thu, 14 May 2026 19:36:37 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf0cfbfef73e4ce590e63f32fa324f98af1783d6550c842d675efb1004954ec`  
		Last Modified: Thu, 14 May 2026 19:36:37 GMT  
		Size: 878.3 KB (878314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff9313ecb7b8bbe58328fa20870d086b775001d49958f6112b62cf99f9093b`  
		Last Modified: Thu, 14 May 2026 19:36:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047b9eec2310e4a3b1289a427365b58ac010876e88e867f0b5161c8ae8e8d8a4`  
		Last Modified: Thu, 14 May 2026 19:36:40 GMT  
		Size: 92.9 MB (92860551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea459165b7825fd80322695fd6d5de692e44e901a711a628c3c915a11d49abd7`  
		Last Modified: Thu, 14 May 2026 19:36:38 GMT  
		Size: 18.9 KB (18924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb330fbfa7dd56efb12b59a8808fb680e3a1975fb228437f54eec86ab8b6ce41`  
		Last Modified: Thu, 14 May 2026 19:36:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c0b23f77babafceeb528df8b100647fc5a4bb2c325fee0a0ad9e1281773072`  
		Last Modified: Thu, 14 May 2026 19:36:39 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d656004310b6e17c06be59c32ddd44e96ace0e161ea14e3a2df59c595d95d185`  
		Last Modified: Thu, 14 May 2026 19:36:40 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:f300136e63021f2d43c604e8352674e9e7089974eceabe1cd21564803bda4b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.8 KB (651777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a584f21c815fecc137d0066ca2b1beaf293ccfe2b0864bfe09feac9af15cdbb`

```dockerfile
```

-	Layers:
	-	`sha256:44049f5b8460f7701d890c29e463575b87d6f437b1e804774c3108cc3f7a5e31`  
		Last Modified: Thu, 14 May 2026 19:36:37 GMT  
		Size: 611.6 KB (611607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4577078b051142f9ad91f6b835baffaef24ca643a3646588b4515642781be591`  
		Last Modified: Thu, 14 May 2026 19:36:37 GMT  
		Size: 40.2 KB (40170 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine3.22` - linux; riscv64

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

### `postgres:18-alpine3.22` - unknown; unknown

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

### `postgres:18-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:b4ee47c4d17963b2451c3e13a3f2da8d040405f427465973a759b7f19a84ef09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122397558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb42f9807f04daca290127c670c0eb59cc933ad1eee24d3d68fee6d269fc4d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 18:56:45 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 18:56:48 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 18:56:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 18:56:48 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 18:56:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 18:56:48 GMT
ENV PG_MAJOR=18
# Thu, 14 May 2026 18:56:48 GMT
ENV PG_VERSION=18.4
# Thu, 14 May 2026 18:56:48 GMT
ENV PG_SHA256=81a81ec695fb0c7901407defaa1d2f7973617154cf27ba74e3a7ab8e64436094
# Thu, 14 May 2026 18:56:48 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 May 2026 18:59:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 May 2026 18:59:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 18:59:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 18:59:48 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 May 2026 18:59:48 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 May 2026 18:59:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 18:59:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 18:59:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 18:59:48 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 18:59:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 18:59:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e81ceb38917acc4cf3d16bd98043e33a3e2c28415750a8e7da557756eba88c`  
		Last Modified: Thu, 14 May 2026 19:00:13 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ba055b6cddec7c6e4795ffdf5ed7ca4139e686e84c442c3304cfa93062746b`  
		Last Modified: Thu, 14 May 2026 19:00:14 GMT  
		Size: 894.2 KB (894241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97aa08e209ba7c6db28b899b90a123a19c5fde82cded0e06cfd0d21184bb0ca7`  
		Last Modified: Thu, 14 May 2026 19:00:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade3213ad1d7c023e409c4d279cc70c06cb55d87e62f914fcd7f208ac974b1d7`  
		Last Modified: Thu, 14 May 2026 19:00:16 GMT  
		Size: 117.8 MB (117823032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdde5405febd58f3de88a98dbf927d2c2e7bba9002d4ffee0560a0cca5a26018`  
		Last Modified: Thu, 14 May 2026 19:00:15 GMT  
		Size: 18.9 KB (18914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20738a1e17094f115797df2d3dc04f76d1e0e8b3ea2a79e154a90f0b02a5e88e`  
		Last Modified: Thu, 14 May 2026 19:00:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9cd412709fb8f3cfde71f1ff6ef1dc39040e8b6246b15e771abbc2205c0c12`  
		Last Modified: Thu, 14 May 2026 19:00:17 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f090143b7dd6a0c0ffbe335b759187c0ee24354ab11a37de0fd35df430ee4b`  
		Last Modified: Thu, 14 May 2026 19:00:17 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:2627a60df3f76b490d5ebbf61fa449780e306b13ff23d8d931e5f59e2163bf1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.4 KB (653366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb756444012773b461caf9b690e1c703cf72e3fce700ab5fcbc752e0e4e9db3`

```dockerfile
```

-	Layers:
	-	`sha256:15957771f586e2e60360665fa7c053b6cb3bfcde9aee9f229cc05f7a5918ed5c`  
		Last Modified: Thu, 14 May 2026 19:00:13 GMT  
		Size: 613.2 KB (613241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1ed12ddc8715b4f9b97d3027c591af6392a8a971047c1c592d47a2049d98138`  
		Last Modified: Thu, 14 May 2026 19:00:13 GMT  
		Size: 40.1 KB (40125 bytes)  
		MIME: application/vnd.in-toto+json
