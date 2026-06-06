## `postgres:19beta1-alpine3.22`

```console
$ docker pull postgres@sha256:8221b309e16fcd0ff409e6291ef265d2944920371dc6330341880e78742f0969
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

### `postgres:19beta1-alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:cb07f43374c4212eba24af99b982c44cc2c61edf40e2ad90d579d1e5557260d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114800070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055695a8a09f79c380e46474043b59cd9a2189e63adeb93cd74e4bdd4359eabe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Sat, 06 Jun 2026 00:20:25 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:20:28 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:20:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:20:28 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:20:28 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:20:28 GMT
ENV PG_VERSION=19beta1
# Sat, 06 Jun 2026 00:20:28 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Sat, 06 Jun 2026 00:20:28 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 06 Jun 2026 00:22:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:22:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:22:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:22:56 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:22:56 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:22:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:22:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:22:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:22:56 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:22:56 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:22:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d3ea9e036b4c09f7413277995cf0d7b67ef0d0b5fb3d78d2e45b0eaa5bd3ad`  
		Last Modified: Sat, 06 Jun 2026 00:23:12 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d26a0e174d580d0d738379c24d9cc669a568d924bdba93bd29be12f80c9273`  
		Last Modified: Sat, 06 Jun 2026 00:23:12 GMT  
		Size: 917.4 KB (917417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd470ae4c82f6292320184ccca37ea362013c0e0f2327b0edcaf08cca646383d`  
		Last Modified: Sat, 06 Jun 2026 00:23:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6d2624d674cb7c9e1253c8be83899a877cb8a56159898f0c81543c754eec34`  
		Last Modified: Sat, 06 Jun 2026 00:23:15 GMT  
		Size: 110.0 MB (110045954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87967e7b054cb03b445855a54a29c0c532890f664f9dda83fc03e5915ef47ccf`  
		Last Modified: Sat, 06 Jun 2026 00:23:13 GMT  
		Size: 21.0 KB (21009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d89573056afeab67a53053fce4fce8657efc54139fe2406a1a45be4dc3fc6e5`  
		Last Modified: Sat, 06 Jun 2026 00:23:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d71766193f20e9c48e46bb10f1958717bdf1adb63c4d08414baa7ac83cffd92`  
		Last Modified: Sat, 06 Jun 2026 00:23:13 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df085c39da8cefe4ec3357fce015199c707852df80d7df779748e474321b5df`  
		Last Modified: Sat, 06 Jun 2026 00:23:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:9659774a73549d8ddaad4ba439c4ce70687603294da1733fe41c300b1b4f8c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.1 KB (654100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f08df7ed816d96535a42fbaacf0111f8fcf250413708b1c5a68bcf92ecb3dab`

```dockerfile
```

-	Layers:
	-	`sha256:30a055b73a0a2541976ee5c8330775ea8c47d656f3f0337937c69d274f3f3664`  
		Last Modified: Sat, 06 Jun 2026 00:23:12 GMT  
		Size: 614.6 KB (614578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49cc18215741228241c29bcc18696756ce4b0650ff6cbde91606329464dcd9f5`  
		Last Modified: Sat, 06 Jun 2026 00:23:11 GMT  
		Size: 39.5 KB (39522 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:408f90de4d078e6d4fdf104f962e47f4663e1e1037ae765fa4415fe922b1e293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94327516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec0357ccdc5d0b24d7736adafc695cd78685e9781c9270b49c61e432abf1c713`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Sat, 06 Jun 2026 00:25:29 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:25:33 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:25:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:25:33 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:25:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:25:33 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:25:33 GMT
ENV PG_VERSION=19beta1
# Sat, 06 Jun 2026 00:25:33 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Sat, 06 Jun 2026 00:25:33 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 06 Jun 2026 00:28:35 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:28:35 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:28:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:28:35 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:28:35 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:28:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:28:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:28:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:28:35 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:28:35 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:28:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ff446a7ffcfdbd94a915cee5b90d92650214d44be89955118d65487185eb74`  
		Last Modified: Sat, 06 Jun 2026 00:28:45 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160b793b0125a3f387dbaaa21a9e543c1ccf5d9e742308ffd11ac1adc8ae9ba6`  
		Last Modified: Sat, 06 Jun 2026 00:28:46 GMT  
		Size: 885.1 KB (885138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a422598233372e0f6274008b29aec00fc34c63190d8e6c3183c96fe0369e59ee`  
		Last Modified: Sat, 06 Jun 2026 00:28:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af219b656189dae09318dfdc31c2787bf61f3d3672697e0cc98bdeed1ef9161b`  
		Last Modified: Sat, 06 Jun 2026 00:28:48 GMT  
		Size: 89.9 MB (89906491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4500a69518840b586314f4fb411bd00186fd22f607b4a8627729b760e4312027`  
		Last Modified: Sat, 06 Jun 2026 00:28:47 GMT  
		Size: 21.0 KB (21006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a84f1d6ccc3ab15edf0300b499c0ad7749dceadd6ec3a30da949637ffcb637`  
		Last Modified: Sat, 06 Jun 2026 00:28:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5cc8a21ac292379e3ecc91e37549b324540b1db6d29bd075777f5138b2e9e2`  
		Last Modified: Sat, 06 Jun 2026 00:28:47 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a16614e5f2d99a0e63363ecd5f31ab4018042be50145d1ec7770216b46b29a9`  
		Last Modified: Sat, 06 Jun 2026 00:28:48 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:b415506d29493635adde4ae03cea8b44d4063df6ee22fc79104c5cbf6c14a879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 KB (39436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f182436e975f062a1e70760ec0d4229d6303aa5b87e82335307d3c36e0a702`

```dockerfile
```

-	Layers:
	-	`sha256:b323aba9c3c6b35ba9d191a3d7597e5620a42029bb3a6da26619757b7027921b`  
		Last Modified: Sat, 06 Jun 2026 00:28:45 GMT  
		Size: 39.4 KB (39436 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:8b16d778b2f38247eea741bd5c248382a90d03428b7d09e999efeaa5081eb7fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89389429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c65c494d3bb92256bf7d605cdc9c51e79500071ab463023836e184e2966125`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Sat, 06 Jun 2026 00:27:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:27:08 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:27:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:27:08 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:27:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:27:08 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:27:08 GMT
ENV PG_VERSION=19beta1
# Sat, 06 Jun 2026 00:27:08 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Sat, 06 Jun 2026 00:27:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 06 Jun 2026 00:30:04 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:30:04 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:30:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:30:04 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:30:04 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:30:04 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:30:04 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:30:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:30:04 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:30:04 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:30:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2006eb7355564dd689bae584242c04fa2a9e367c9029c44d5cda3149cf0cb02`  
		Last Modified: Sat, 06 Jun 2026 00:30:16 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce68d81f1e535c2357b84f7a396471b7f3c5b1128d9b4c40a638b315d5f3e01d`  
		Last Modified: Sat, 06 Jun 2026 00:30:17 GMT  
		Size: 885.1 KB (885150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb62a6564d574af48289037558ea2b223d1f059c8046d64d518a8192e7ec87d`  
		Last Modified: Sat, 06 Jun 2026 00:30:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927736f379f3c04f09c6b440e36b6d3b5dd4981f37c3633aafc5e411eb476638`  
		Last Modified: Sat, 06 Jun 2026 00:30:19 GMT  
		Size: 85.2 MB (85249946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdee16c083a6ec68208d870f5df103456cc338bf78482dbfcd3c628dafa3e4e`  
		Last Modified: Sat, 06 Jun 2026 00:30:17 GMT  
		Size: 21.0 KB (21004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e8eceeb9044d43cb48849274c648def4270dd87a2d1d6d4d7bb2c75365d414`  
		Last Modified: Sat, 06 Jun 2026 00:30:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cda414e76fd1e6795719883ea189d2ead7452380148a931465cecba2fea578`  
		Last Modified: Sat, 06 Jun 2026 00:30:18 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26777f8bc338f9c7d7475c5d21b48b27f0085dce76e4b36ebec762b55fda983a`  
		Last Modified: Sat, 06 Jun 2026 00:30:19 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:6d7ac2b9f33607bd824def58a103c3d71116300617a66072314a9b269c7a7597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.2 KB (654241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a304b9a47e96f91a8bd99a4eee23c22accb76074b5bd68fb2730161a67f349`

```dockerfile
```

-	Layers:
	-	`sha256:bd9769d770339c4854a2b3a60d8b44a1c6149388a53c00f45ba4c52554c2ee93`  
		Last Modified: Sat, 06 Jun 2026 00:30:16 GMT  
		Size: 614.6 KB (614590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f844cec4a8993b9ed5858bed6e5a44b53306935800fcdb5ea89cc1115ebe7e9e`  
		Last Modified: Sat, 06 Jun 2026 00:30:16 GMT  
		Size: 39.7 KB (39651 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:dffa1497ee49578bcf771959690b497522598a4c71ce2dbc0df68f134bf9af3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110733579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bafc1e2638d4b6cc978aa8459a9c0bdacc5f73b7948ec0f9bcc5b6de899b1879`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Sat, 06 Jun 2026 00:21:51 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:21:54 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:21:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:21:54 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:21:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:21:54 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:21:54 GMT
ENV PG_VERSION=19beta1
# Sat, 06 Jun 2026 00:21:54 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Sat, 06 Jun 2026 00:21:54 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 06 Jun 2026 00:24:27 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:24:27 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:24:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:24:28 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:24:28 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:24:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:24:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:24:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:24:28 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:24:28 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:24:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c191d251df042da2cb2b1e5fa0f9ec46f72a449d43671f12a99f3e5d27ef32`  
		Last Modified: Sat, 06 Jun 2026 00:24:42 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db40d1fef9373d521c93a5f5a4f1dd1acc314679ec9b81cd17a868fb5b3af1a3`  
		Last Modified: Sat, 06 Jun 2026 00:24:43 GMT  
		Size: 873.1 KB (873121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cfdf760f69c77b41cc5ff1386f0254358c5994b1625af9bbe94250b5aa1316`  
		Last Modified: Sat, 06 Jun 2026 00:24:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0811a26287f02342157dc92b0ea36a7d01be2c5b0b5f9e82726bcf7af714c16a`  
		Last Modified: Sat, 06 Jun 2026 00:24:45 GMT  
		Size: 105.7 MB (105690056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cdea934e3043862fa85108e3148db99b12362df975ba80e386208130ecf7e6`  
		Last Modified: Sat, 06 Jun 2026 00:24:44 GMT  
		Size: 21.0 KB (21006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e16ab9a3e66dabff9aeff618831d7124778dd615a93daa35086a510e759ed6e`  
		Last Modified: Sat, 06 Jun 2026 00:24:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0142ec76e2cd499a0a6cba107c161e5ff4cf4ecede927cc5c36c28cee045902b`  
		Last Modified: Sat, 06 Jun 2026 00:24:44 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604ede1d3b55027d7a76a6d78f7a3151305b34937995d58c50b74d06fbdd22f2`  
		Last Modified: Sat, 06 Jun 2026 00:24:45 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:102157b35ca62389b965ba7a7a65508a631c3ce64087dce8ae57c833ff58a1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.3 KB (654278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988f260226705dc35e8c4edd49550baf3be1709de2a061ba321611335d4bfe23`

```dockerfile
```

-	Layers:
	-	`sha256:fa70d3307918182ca2f125e6ed8cf90a5fc9e7950c72418d206a0d3264eab240`  
		Last Modified: Sat, 06 Jun 2026 00:24:43 GMT  
		Size: 614.6 KB (614598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:673bc8f98bcccaf23ba4ea692629daeff229444b4456ac138ac215e0014a11d5`  
		Last Modified: Sat, 06 Jun 2026 00:24:42 GMT  
		Size: 39.7 KB (39680 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:99d680fb3ea7f25e46d733868dc589098b164f09625519e3f5a24327692530bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121317193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ae08b259b169bb144e1cae8edf6de3508ac286629a91237b21fd5f4c291656`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Sat, 06 Jun 2026 00:21:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:21:33 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:21:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:21:33 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:21:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:21:33 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:21:33 GMT
ENV PG_VERSION=19beta1
# Sat, 06 Jun 2026 00:21:33 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Sat, 06 Jun 2026 00:21:33 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 06 Jun 2026 00:24:33 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:24:33 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:24:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:24:33 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:24:33 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:24:33 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:24:33 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:24:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:24:33 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:24:33 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:24:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da85f0189fd2aa9c6f7d7f1b4a3db3c5b8f62887160a0b144e58a4de05a15c4c`  
		Last Modified: Sat, 06 Jun 2026 00:24:49 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99168b555e0e41591d1dc834be241db16817d7a5b9fb1c5ea00e6a0360a4ecbc`  
		Last Modified: Sat, 06 Jun 2026 00:24:50 GMT  
		Size: 889.8 KB (889751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98addc9915f9f76269e48045b9a6106dac3e6559cc4fc6fc111129b4f933f49a`  
		Last Modified: Sat, 06 Jun 2026 00:24:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51495fafac18c43261a58e996773abb7051d721e0f0ef0f27f86e4590c93e87c`  
		Last Modified: Sat, 06 Jun 2026 00:24:54 GMT  
		Size: 116.8 MB (116774222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f627ddb3411496c0e875f11be122bc7a335969b95562d56564241b6f08d01637`  
		Last Modified: Sat, 06 Jun 2026 00:24:51 GMT  
		Size: 21.0 KB (21004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c37687c0b427bc9b662886e1d1b91cfe6335d79be45c90c43ee331677a088b`  
		Last Modified: Sat, 06 Jun 2026 00:24:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e39d0855620d3a4a02fd26f7ab11682925569fd2156f5d41c1a99a14b2abe1d`  
		Last Modified: Sat, 06 Jun 2026 00:24:52 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdc4435874c56173d12f12ec9fb946d4876befc84383c063ecf4c1ac897031b`  
		Last Modified: Sat, 06 Jun 2026 00:24:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:52089b877cb8650a3ad6cd5e91b47f2452a09b88b54a437d8a7ff7519c360b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.1 KB (654061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9908b45499da7fbe84d2c24be1624620302b279c34b142874e6db5b36f136b75`

```dockerfile
```

-	Layers:
	-	`sha256:7837b111e8e10d687438f72ac11fa3d2dddf18cd2ea77e9159a7659edf35c778`  
		Last Modified: Sat, 06 Jun 2026 00:24:50 GMT  
		Size: 614.6 KB (614568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d83d5bc620ec5995bc8f70f3cce245e7e9eff864ffca8ee546b5be8c30728c0`  
		Last Modified: Sat, 06 Jun 2026 00:24:49 GMT  
		Size: 39.5 KB (39493 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:057b2f8369d3bf2c84631dcde12a3196cc2c35d892c1a5ae3bb3923b15de7139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98883031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b0eddff4eb71211efc9032f64409bb4d251567577297451d7a1651718463d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
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
# Sat, 06 Jun 2026 01:12:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 06 Jun 2026 01:12:07 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 01:12:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 01:12:08 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 01:12:08 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 01:12:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 01:12:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 01:12:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 01:12:09 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 01:12:09 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 01:12:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb9d4257b97ccac764de9a825ba0167620e376c6dd166a6d9be2cd3a44e35e`  
		Last Modified: Sat, 06 Jun 2026 01:12:38 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2306f66a05e739adebd693d60349d778a9b2f4c0c3d3f2f8a463262fb54a2a`  
		Last Modified: Sat, 06 Jun 2026 01:12:38 GMT  
		Size: 878.3 KB (878317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c5f90bd0fef1b1501e2e84ee0db1b7c002dc18ab2d13d4467a6742cbecaf3b`  
		Last Modified: Sat, 06 Jun 2026 01:12:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2b21f7ecff5dbc87a891202c89d7480a0e707b80d623067648411af85f8b3f`  
		Last Modified: Sat, 06 Jun 2026 01:12:40 GMT  
		Size: 94.2 MB (94239549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a49eaa02eef54250d864683aa7be17a37d0a113010024c53f032e2878df224d`  
		Last Modified: Sat, 06 Jun 2026 01:12:39 GMT  
		Size: 21.0 KB (21009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bb07b13b1d4cce9da9edee3c8167ae2b122843e481639e2ba343816f791348`  
		Last Modified: Sat, 06 Jun 2026 01:12:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41077453c8614a2003f8eb685186816bdf73b92d42e6be740528f491816ae9a3`  
		Last Modified: Sat, 06 Jun 2026 01:12:40 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd25bd8a2ed20f57fb040deb836937e56040505fb652ea368095e51b81eea2a`  
		Last Modified: Sat, 06 Jun 2026 01:12:41 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:85eb4c9e81febea970faae2678fb3c5a5e584e998f1063d34111c91d528a1170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.5 KB (650536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb23425e5671d4eedb246cebe6cc82ad8a26d55558e6cc2adf734544eaf09010`

```dockerfile
```

-	Layers:
	-	`sha256:9062f52629c4f3c9b981d531c7b10f7a08d6b6be504d77803ea6cd5d74221d36`  
		Last Modified: Sat, 06 Jun 2026 01:12:38 GMT  
		Size: 611.0 KB (610981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d30e10a9065ab5dff46fce767e1497e4a879292a92f2f64e407640baf9e4ea21`  
		Last Modified: Sat, 06 Jun 2026 01:12:38 GMT  
		Size: 39.6 KB (39555 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:19beta1-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:c402e81701eba92a1b2b26fcf0e747215d6fc5dd157a91d579101e14f630a287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123724001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4493be66e5856c0a5b1f0d8e4e12801ac94b6b554d9f9d084a336f06c8b3784`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Sat, 06 Jun 2026 00:30:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:30:47 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:30:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:30:47 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:30:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:30:47 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:30:47 GMT
ENV PG_VERSION=19beta1
# Sat, 06 Jun 2026 00:30:47 GMT
ENV PG_SHA256=d8c8d3e18c12e9fb792b3e927049900d40571f4ef6167017a23e5bbfc40d30ee
# Sat, 06 Jun 2026 00:30:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 06 Jun 2026 00:34:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:34:07 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:34:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:34:07 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:34:07 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:34:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:34:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:34:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:34:07 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:34:07 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:34:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7410025bc28a84b359164862608c3dc3aae16bd6207e76e6a3ffd958f625d1e`  
		Last Modified: Sat, 06 Jun 2026 00:34:33 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625e8deb5ac899410b2071a3d244ef3a6b3a9a870b36b1ab4dec9dcaaae6ca9e`  
		Last Modified: Sat, 06 Jun 2026 00:34:33 GMT  
		Size: 894.2 KB (894246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7af9c40cfbae75940fdc86cb3f2eb509fe086b5a3aae588e4b46975c9270d9`  
		Last Modified: Sat, 06 Jun 2026 00:34:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9defe280edd80f001693077b778f8b323672f62770b2ece2dd0167193abc94b7`  
		Last Modified: Sat, 06 Jun 2026 00:34:35 GMT  
		Size: 119.1 MB (119147379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae05fdff0cd2b4115c9b50419d701175068e120494a0243bbc780eaae1196690`  
		Last Modified: Sat, 06 Jun 2026 00:34:34 GMT  
		Size: 21.0 KB (21006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51924ea57c7b7fa38f2d13497a9c4db77442d9659a315adfb97abb9a26e0dbc`  
		Last Modified: Sat, 06 Jun 2026 00:34:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f38367e8057b55c0168cbbcf2c054c6140d3ac1ad0728cc5af8ada6e4209c22`  
		Last Modified: Sat, 06 Jun 2026 00:34:34 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841823b48f2d183a8c0c75588acbe2dda1f3e038f3fa945b0e30a8c8db677ded`  
		Last Modified: Sat, 06 Jun 2026 00:34:35 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:d7dd6d53d7f918a1b3e989a8347e1e9f3b01ce10969822fc5d124712bd8103d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **652.1 KB (652149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57d5c33cf7446be1ce06ef9d97516427875bc039a1588007919047a6f55de42`

```dockerfile
```

-	Layers:
	-	`sha256:b22acd8c98f9529b7af99d35d446d34fa0b08e79f480fc10be0b0ff3232e9c6e`  
		Last Modified: Sat, 06 Jun 2026 00:34:33 GMT  
		Size: 612.6 KB (612627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b952c8c4ba3c022755bad654b1cfc5994185ca1343b6dcac943422b561aefd`  
		Last Modified: Sat, 06 Jun 2026 00:34:33 GMT  
		Size: 39.5 KB (39522 bytes)  
		MIME: application/vnd.in-toto+json
