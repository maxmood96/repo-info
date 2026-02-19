## `postgres:18-alpine`

```console
$ docker pull postgres@sha256:035b9ab53cfa147d7202b61f5f7782b939ae815b7d6bc81c96b7b42ff1fca950
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

### `postgres:18-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:9560e8419a4918b86a54703cebcb0c89c59b741ee2461761352336df09bacb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (114001349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6f6fbdba22639c7670937cf3fd94d5cf2c6a8edf3751db574b333cd089297c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 23:35:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 18 Feb 2026 23:35:19 GMT
ENV GOSU_VERSION=1.19
# Wed, 18 Feb 2026 23:35:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 18 Feb 2026 23:35:19 GMT
ENV LANG=en_US.utf8
# Wed, 18 Feb 2026 23:35:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 18 Feb 2026 23:35:19 GMT
ENV PG_MAJOR=18
# Wed, 18 Feb 2026 23:35:19 GMT
ENV PG_VERSION=18.2
# Wed, 18 Feb 2026 23:35:19 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Wed, 18 Feb 2026 23:35:19 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 18 Feb 2026 23:37:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 18 Feb 2026 23:37:42 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 18 Feb 2026 23:37:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 18 Feb 2026 23:37:42 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 18 Feb 2026 23:37:42 GMT
VOLUME [/var/lib/postgresql]
# Wed, 18 Feb 2026 23:37:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 23:37:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 18 Feb 2026 23:37:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 23:37:42 GMT
STOPSIGNAL SIGINT
# Wed, 18 Feb 2026 23:37:42 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 18 Feb 2026 23:37:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f877ddb15ca43c1bf256739ac5c1cd307bf9fbfa64eb4371d2e73d71cf4b5a`  
		Last Modified: Wed, 18 Feb 2026 23:37:57 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fd599ecd5133145223a9cd7f1b173eab0854a09e90c51805674d797fae1f06`  
		Last Modified: Wed, 18 Feb 2026 23:37:57 GMT  
		Size: 922.9 KB (922940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c93a3f7fc721c9b9aadcca0e4746fde5965be41994f6a6e21604274b201e165`  
		Last Modified: Wed, 18 Feb 2026 23:37:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e59f79710f333535dd1de41b81cb26ffbf01b552c6128567dc798ecfe96e2aa`  
		Last Modified: Wed, 18 Feb 2026 23:38:00 GMT  
		Size: 109.2 MB (109190419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d0e9c026d83b37aef7c62b7a9bac4bce098f1c873711ba3f606e24af1673c1`  
		Last Modified: Wed, 18 Feb 2026 23:37:58 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3c0b82e14f6efacfdcdfe408f2827be1ce4a3a4134184358d4cc6c68214a77`  
		Last Modified: Wed, 18 Feb 2026 23:37:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4dfe0d66a6ccfb01f3077d6627092564dbc1d9d1039a86774ec4650a35ee66`  
		Last Modified: Wed, 18 Feb 2026 23:37:59 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d23faa6dee53fb4edb679feecda9152eacce551290774b2c7c12ddd3c2e2977`  
		Last Modified: Wed, 18 Feb 2026 23:37:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:39a29b17b80630fe2bbe0dc352d1d37d477bf9598ee2ff9f54228bb0654a07e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.9 KB (659946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2a6faea0df55dffa3ff0360a7cf68334da83df89d5f16befea135a677417c6`

```dockerfile
```

-	Layers:
	-	`sha256:6263bed513d63ed970814a67c7653c54799bbe8ffdbe421227200c3a01150a3c`  
		Last Modified: Wed, 18 Feb 2026 23:37:57 GMT  
		Size: 618.9 KB (618898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36855dfd1f0923f4cd2a2752fa4f745c327733efe6c9f6a18cf752c634add63a`  
		Last Modified: Wed, 18 Feb 2026 23:37:57 GMT  
		Size: 41.0 KB (41048 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:56265ef67230b2aba55a0f31b16b3126d6f6cf9aa23bb1e3abf84df3739c9393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93383927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35fc8d23a93fc2e9c63b606f67c47e800a459e93c9a6b567dc937358830e44ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 23:36:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 18 Feb 2026 23:36:36 GMT
ENV GOSU_VERSION=1.19
# Wed, 18 Feb 2026 23:36:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 18 Feb 2026 23:36:36 GMT
ENV LANG=en_US.utf8
# Wed, 18 Feb 2026 23:36:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 18 Feb 2026 23:36:36 GMT
ENV PG_MAJOR=18
# Wed, 18 Feb 2026 23:36:36 GMT
ENV PG_VERSION=18.2
# Wed, 18 Feb 2026 23:36:36 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Wed, 18 Feb 2026 23:36:36 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 18 Feb 2026 23:39:26 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 18 Feb 2026 23:39:27 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 18 Feb 2026 23:39:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 18 Feb 2026 23:39:27 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 18 Feb 2026 23:39:27 GMT
VOLUME [/var/lib/postgresql]
# Wed, 18 Feb 2026 23:39:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 23:39:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 18 Feb 2026 23:39:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 23:39:27 GMT
STOPSIGNAL SIGINT
# Wed, 18 Feb 2026 23:39:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 18 Feb 2026 23:39:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f379f6705399fee31de0e9d57270a10283126876d4da980f940331c9460ed5bd`  
		Last Modified: Wed, 18 Feb 2026 23:39:37 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d801f6e2b6cb7400605fa5f0362105c5ef25863e5ad87a544ac87e0030161502`  
		Last Modified: Wed, 18 Feb 2026 23:39:37 GMT  
		Size: 889.5 KB (889468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b1a56ad3332c6fc07c26a69eb176f31832a2bdf387d11c3511ad09287466b0`  
		Last Modified: Wed, 18 Feb 2026 23:39:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec2a5b164605870b92482af9d6944ea095e078e4b4af28883f775ca12c93d6b`  
		Last Modified: Wed, 18 Feb 2026 23:39:40 GMT  
		Size: 88.9 MB (88898486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79101f6c33539e298338dafc9c250262b33d94f7df53d5111e208df561a8110`  
		Last Modified: Wed, 18 Feb 2026 23:39:38 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fceed892a6e23996472c3935afef8eb860e24599a3c246d34ba7a10a6b8e73b`  
		Last Modified: Wed, 18 Feb 2026 23:39:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a15c522688be885205bca254dbeeb53ecc88d150e64aec682998b68718e297f`  
		Last Modified: Wed, 18 Feb 2026 23:39:39 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc57135224c9f789eee8a42ecfc4ccab4c53409024a0350c12b2ff95769532f`  
		Last Modified: Wed, 18 Feb 2026 23:39:39 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:e48dc2ee5430af6310138382305df83a14ef1d3266607eb51f52bc5d7561be6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 KB (41002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5d50925a25fe11b1345f546bacb8abbc65b8ff4174fe23e022d14956adc80b`

```dockerfile
```

-	Layers:
	-	`sha256:db3bcdcb25778c9cbb771c1d6d28045670ef21e80be9b52cd83fb78bbe717611`  
		Last Modified: Wed, 18 Feb 2026 23:39:37 GMT  
		Size: 41.0 KB (41002 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:eb0cd5e335d4262b871d33f794f6238e323456c31f05d5ca098561a12ac6401e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88461171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7f90faf1fcfc60909e273aa933c5772f4fdc693ea4c1e7310d97cfd45c11d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 23:35:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 18 Feb 2026 23:35:17 GMT
ENV GOSU_VERSION=1.19
# Wed, 18 Feb 2026 23:35:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 18 Feb 2026 23:35:17 GMT
ENV LANG=en_US.utf8
# Wed, 18 Feb 2026 23:35:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 18 Feb 2026 23:35:17 GMT
ENV PG_MAJOR=18
# Wed, 18 Feb 2026 23:35:17 GMT
ENV PG_VERSION=18.2
# Wed, 18 Feb 2026 23:35:17 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Wed, 18 Feb 2026 23:35:17 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 18 Feb 2026 23:38:11 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 18 Feb 2026 23:38:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 18 Feb 2026 23:38:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 18 Feb 2026 23:38:11 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 18 Feb 2026 23:38:11 GMT
VOLUME [/var/lib/postgresql]
# Wed, 18 Feb 2026 23:38:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 23:38:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 18 Feb 2026 23:38:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 23:38:11 GMT
STOPSIGNAL SIGINT
# Wed, 18 Feb 2026 23:38:11 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 18 Feb 2026 23:38:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8511290c38f364c6b2cbff0eb71a8088cb78739f24eef56549e3a53df01f8691`  
		Last Modified: Wed, 18 Feb 2026 23:38:23 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6f2c2f1c06507caf222ed3063f5f99c9d7192292fb653356b7299364f2f930`  
		Last Modified: Wed, 18 Feb 2026 23:38:23 GMT  
		Size: 889.5 KB (889511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52b8bb12ffb46364a26dee77dc15c72dcfa001ef0542deae1b748347f08a176`  
		Last Modified: Wed, 18 Feb 2026 23:38:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b8c08cbb7f18710ef418ce48be8eb25fb10c23c95bc7f817177727f013e82a`  
		Last Modified: Wed, 18 Feb 2026 23:38:25 GMT  
		Size: 84.3 MB (84263783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a0365033193b3752b7d59adca290343cdb02ab5198df83ba6fed3dbe11620d`  
		Last Modified: Wed, 18 Feb 2026 23:38:24 GMT  
		Size: 18.9 KB (18918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c699478e1c2b70aa92b3e1bdb165250a56c834ccdfb47920346144bc4cd541`  
		Last Modified: Wed, 18 Feb 2026 23:38:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a33bb907b9d88700be6a97b7fbe5478237618407becce29442f1c206599ad7`  
		Last Modified: Wed, 18 Feb 2026 23:38:25 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672f025906e1ce4212d6dc0a62b2e83a67cfa48d857d5f71b692d8babb89edb`  
		Last Modified: Wed, 18 Feb 2026 23:38:25 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:d89177ba916136219fb2d23e393a1ee0c55c06153e2af37de9e0bc0b5f413d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.5 KB (659517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc7ca9364452f13a7c32dd9768b813a2998df8ab9213d6e22aca1afd971b42e`

```dockerfile
```

-	Layers:
	-	`sha256:20c6a4cf75e603cac9a2709b11e7dd14be163bf705b63b11bede5b874a6c73be`  
		Last Modified: Wed, 18 Feb 2026 23:38:23 GMT  
		Size: 618.3 KB (618300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a87179009630b9a473d3de49a488e47b5d2d3be7097ab3545d2e796bf7c9e82e`  
		Last Modified: Wed, 18 Feb 2026 23:38:23 GMT  
		Size: 41.2 KB (41217 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:699296dc1ca93a0543e36a150c100e47844154e53e50a087fa994bea2f1dcc35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112203953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97357d492d16333a6f046b8100bc410616bade586e4435e32213b235625aeb01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 23:35:10 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 18 Feb 2026 23:35:13 GMT
ENV GOSU_VERSION=1.19
# Wed, 18 Feb 2026 23:35:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 18 Feb 2026 23:35:13 GMT
ENV LANG=en_US.utf8
# Wed, 18 Feb 2026 23:35:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 18 Feb 2026 23:35:13 GMT
ENV PG_MAJOR=18
# Wed, 18 Feb 2026 23:35:13 GMT
ENV PG_VERSION=18.2
# Wed, 18 Feb 2026 23:35:13 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Wed, 18 Feb 2026 23:35:13 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 18 Feb 2026 23:37:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 18 Feb 2026 23:37:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 18 Feb 2026 23:37:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 18 Feb 2026 23:37:37 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 18 Feb 2026 23:37:37 GMT
VOLUME [/var/lib/postgresql]
# Wed, 18 Feb 2026 23:37:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 23:37:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 18 Feb 2026 23:37:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 23:37:37 GMT
STOPSIGNAL SIGINT
# Wed, 18 Feb 2026 23:37:37 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 18 Feb 2026 23:37:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f67ec7335baf4de11b346fa8e3eae82b01e03f428b2186f24caa54d498cf4e`  
		Last Modified: Wed, 18 Feb 2026 23:37:52 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b221dbefc5cb2a666050bae3720841d6dcd933d68021e84b6806fbf36a87fe`  
		Last Modified: Wed, 18 Feb 2026 23:37:52 GMT  
		Size: 876.5 KB (876492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dcb098f0424db821d69b94a30062683e5e568e39d7a4a1ba61a2020a6ede35`  
		Last Modified: Wed, 18 Feb 2026 23:37:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfad213ab702ab5797f0b8974f86ecf1bb3110ec7a5cd1984b52daabd1c1c105`  
		Last Modified: Wed, 18 Feb 2026 23:37:55 GMT  
		Size: 107.1 MB (107104210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b73fc0b7653b1ec50eb1d8bb5c9ef56d68bf49ff816d97c19297300e831b44`  
		Last Modified: Wed, 18 Feb 2026 23:37:54 GMT  
		Size: 18.9 KB (18921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908798ff3f9dcf108fd56a269de39ed2a4ce4e2de42b02a94e79e0d4c68a63a`  
		Last Modified: Wed, 18 Feb 2026 23:37:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c9e6970193064dc05a7da0cab1e2944110c87a8407814f8f1cab099cfe5c8d`  
		Last Modified: Wed, 18 Feb 2026 23:37:54 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a678cfc0e63062e6c05f4b243d16147c677110030a4b98b7df1e8d64fdd9394`  
		Last Modified: Wed, 18 Feb 2026 23:37:55 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:4088a7131d99304f80e42863ad95c6a2c4b8eb15e255bbc3045c9345e85f5c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.6 KB (659593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4753e406f1ac66fcf0bac357f473d82166d69fdc34c613f1320d976afba3ded8`

```dockerfile
```

-	Layers:
	-	`sha256:bb17a84dab24bea8535be940a01838bcfa9f143d996db49497a9e4ffeb907993`  
		Last Modified: Wed, 18 Feb 2026 23:37:52 GMT  
		Size: 618.3 KB (618328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52e67967a6e1a53b61cbf5959b5b1139c51530a6497cd4e4615df991768ed619`  
		Last Modified: Wed, 18 Feb 2026 23:37:52 GMT  
		Size: 41.3 KB (41265 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine` - linux; 386

```console
$ docker pull postgres@sha256:aae43be0a2a90f8aa9187eef72d6006ff60d090a786e87500bb2d2d480e7a9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120189840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b631586079ddaa4010f2e46cbdcdf43d7dcee2c8c351c2a42a8007d608bd46e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 23:35:48 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 18 Feb 2026 23:35:51 GMT
ENV GOSU_VERSION=1.19
# Wed, 18 Feb 2026 23:35:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 18 Feb 2026 23:35:51 GMT
ENV LANG=en_US.utf8
# Wed, 18 Feb 2026 23:35:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 18 Feb 2026 23:35:52 GMT
ENV PG_MAJOR=18
# Wed, 18 Feb 2026 23:35:52 GMT
ENV PG_VERSION=18.2
# Wed, 18 Feb 2026 23:35:52 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Wed, 18 Feb 2026 23:35:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 18 Feb 2026 23:38:53 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 18 Feb 2026 23:38:53 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 18 Feb 2026 23:38:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 18 Feb 2026 23:38:53 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 18 Feb 2026 23:38:53 GMT
VOLUME [/var/lib/postgresql]
# Wed, 18 Feb 2026 23:38:53 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 23:38:53 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 18 Feb 2026 23:38:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 23:38:53 GMT
STOPSIGNAL SIGINT
# Wed, 18 Feb 2026 23:38:53 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 18 Feb 2026 23:38:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b8788e1433ea086f51fa15f9d0b5db2f6e50927e1da5e69772f5cd75236030`  
		Last Modified: Wed, 18 Feb 2026 23:39:10 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2528ac40a7e095253c9713e205c5039a7c2c376a3bd13d82b0180bf798874ab5`  
		Last Modified: Wed, 18 Feb 2026 23:39:10 GMT  
		Size: 893.3 KB (893254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06d75ccbddcc564fb73d40e3c13e19f3fcc32fd676533b0b8d41ee081aee540`  
		Last Modified: Wed, 18 Feb 2026 23:39:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b03d4262d0ed87e0dc8edefcca5bc690f51b6d4e2a426f367a5372bb03cc285`  
		Last Modified: Wed, 18 Feb 2026 23:39:13 GMT  
		Size: 115.6 MB (115583431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c340da5d3fabadd4cdfbd715337f8618c0a993354a27cb3bb879ff011372a036`  
		Last Modified: Wed, 18 Feb 2026 23:39:11 GMT  
		Size: 18.9 KB (18919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca7f2a89b5fd7834cb4a40ffa3e06b955e2f0d5bdf1e4cca72cf08ee0f0949e`  
		Last Modified: Wed, 18 Feb 2026 23:39:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66775a367fae08a408609426cc473f498b7bc7836097153e50554c532735956`  
		Last Modified: Wed, 18 Feb 2026 23:39:12 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d205e7f8c77fe485950c0e7ee8a228e161944af7643fd58a97b597050d4cf1`  
		Last Modified: Wed, 18 Feb 2026 23:39:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:68e546e8f257ec5fc12fa353080efbd406c61e841bc17555f54eaf0c30e9a70e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.9 KB (659857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8fd0527af9bdac1abc895de589ce614fe979bb8050a5df44da66a73bd4f800`

```dockerfile
```

-	Layers:
	-	`sha256:63b116f79a68a47b604f37bb1928def9aa34aaac90f60ed9cd4b1ee7da89096d`  
		Last Modified: Wed, 18 Feb 2026 23:39:10 GMT  
		Size: 618.9 KB (618863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba8644578741d8dad19d847f7ae6be317bd89a1f2d32841136d795193b247c0`  
		Last Modified: Wed, 18 Feb 2026 23:39:10 GMT  
		Size: 41.0 KB (40994 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:a3c1923f5d7c1b8221f094a685e6cccb715badb263ecc17c2935380e61f21410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99195647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085c581d509c64ff5fcb7f9c9571746e4743eba616715e4bee77fb5cb7fbeae2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 21:05:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:05:44 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:05:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:05:44 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:05:45 GMT
ENV PG_MAJOR=18
# Thu, 12 Feb 2026 21:05:45 GMT
ENV PG_VERSION=18.2
# Thu, 12 Feb 2026 21:05:45 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Thu, 12 Feb 2026 21:05:45 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 18 Feb 2026 23:39:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 18 Feb 2026 23:39:33 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 18 Feb 2026 23:39:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 18 Feb 2026 23:39:33 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 18 Feb 2026 23:39:33 GMT
VOLUME [/var/lib/postgresql]
# Wed, 18 Feb 2026 23:39:34 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 23:39:34 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 18 Feb 2026 23:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 23:39:34 GMT
STOPSIGNAL SIGINT
# Wed, 18 Feb 2026 23:39:34 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 18 Feb 2026 23:39:34 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3303791000843bb87e4139ec69d0072bf49042341568a87e31e34fee9bb6b8d`  
		Last Modified: Thu, 12 Feb 2026 21:10:41 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b84c177f4fdd062892cae0bf053756f85b594952f273a772df42fab740e47f3`  
		Last Modified: Thu, 12 Feb 2026 21:10:41 GMT  
		Size: 881.5 KB (881516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534e5f4d716482771a39a20177f453ef047051c561f910571baac7b1842baf6d`  
		Last Modified: Thu, 12 Feb 2026 21:10:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6492574e094d1cb6118000e6b8b9a4ab35a3075f69ae72afb1021dbc07dc3f04`  
		Last Modified: Wed, 18 Feb 2026 23:40:24 GMT  
		Size: 94.5 MB (94458321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0c423493f14cfd6c5aa0b779a67c19d04ce058a6bb7916aa36883b80269f44`  
		Last Modified: Wed, 18 Feb 2026 23:40:22 GMT  
		Size: 18.9 KB (18925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb26c2fe8d90f4656a41abca994797387ab7a8212a5fde361318bcde5c62ad17`  
		Last Modified: Wed, 18 Feb 2026 23:40:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f78e42884ecbd0e350d04de135173fcb8df0ec5547ddb4aa701953fa96b442e`  
		Last Modified: Wed, 18 Feb 2026 23:40:22 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef559031b9afe54bc89442daaba641c8341116d35254aac2379989a958b42e3`  
		Last Modified: Wed, 18 Feb 2026 23:40:23 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:94d03381df4542da7e95b458b1ce6c672a078636bc7ebf75ba7613e45083657c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.7 KB (657741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf2f1a6f71f9fced3c7611fa2236b06fafc713908bcb736f6b44ffa09ff39ff`

```dockerfile
```

-	Layers:
	-	`sha256:b4da721a7f1e63d9956c2b10437896379b49d412226ccfb8d188e93094767722`  
		Last Modified: Wed, 18 Feb 2026 23:40:22 GMT  
		Size: 616.6 KB (616631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b08957819ebc6a193f5ef5f54d7eb397f54392b778034f202f3b8db0aa3211f`  
		Last Modified: Wed, 18 Feb 2026 23:40:22 GMT  
		Size: 41.1 KB (41110 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:10570943dbc7a471b81528c70060b29159e46372d7840b6e5e9bcb942988bdee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115346131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb28c3a1b7bf3a015ec5d0231a872bf777cba023ad979552eb94680e73e3ef9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 12 Feb 2026 23:08:51 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 23:09:02 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 23:09:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 23:09:02 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 23:09:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 23:09:03 GMT
ENV PG_MAJOR=18
# Thu, 12 Feb 2026 23:09:03 GMT
ENV PG_VERSION=18.2
# Thu, 12 Feb 2026 23:09:03 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Thu, 12 Feb 2026 23:09:03 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 19 Feb 2026 00:26:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 19 Feb 2026 00:26:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 19 Feb 2026 00:26:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 19 Feb 2026 00:26:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 19 Feb 2026 00:26:06 GMT
VOLUME [/var/lib/postgresql]
# Thu, 19 Feb 2026 00:26:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 19 Feb 2026 00:26:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 19 Feb 2026 00:26:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Feb 2026 00:26:07 GMT
STOPSIGNAL SIGINT
# Thu, 19 Feb 2026 00:26:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 19 Feb 2026 00:26:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4bf1089e3e4046b2263b0510bf148b29c663632753f3b12c015812638b3c1d`  
		Last Modified: Fri, 13 Feb 2026 00:02:06 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a22e9ae65cd8952ab5dcd13b337378c807b8c993fc757a882f6e64d9aa5fea`  
		Last Modified: Fri, 13 Feb 2026 00:02:06 GMT  
		Size: 868.9 KB (868941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8148b66fa8f993f7a3afc5dd362babe771ef176b9fd9d740a885b2f05b45d05`  
		Last Modified: Fri, 13 Feb 2026 00:02:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a976776641631be329bb1c9be70d3734ef17c8d29b676d79a41d546108e3863f`  
		Last Modified: Thu, 19 Feb 2026 00:29:22 GMT  
		Size: 110.9 MB (110865740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195bb281bb1f9cfba65ffecc7064b26499bc2a7e5b255a02ce2eb450d9029725`  
		Last Modified: Thu, 19 Feb 2026 00:29:05 GMT  
		Size: 18.9 KB (18920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae1a4c17725499a1c8591e8b992fd65b144c20e983411cb1915d582665d200a`  
		Last Modified: Thu, 19 Feb 2026 00:29:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13333299e701d7e9dd62b9c0c3dcbc6700c2680250560a01d806e87c0b34fad`  
		Last Modified: Thu, 19 Feb 2026 00:29:05 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edca444f945bea7676f20f5d0f4cf89fc2d6ca2415bbcc036c71831bc0dbcbfc`  
		Last Modified: Thu, 19 Feb 2026 00:29:07 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:50ec16223655b708c594719a4a66cdbfa0949e60d040ac186617e9ffa0950f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.4 KB (659405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba315583f37bc1c7dbd59e1508049882fa10d5429aebcbb98fde1829f8d454b7`

```dockerfile
```

-	Layers:
	-	`sha256:c2d32c064b175696785ffbd1f0d69701a12272de646e1b827b24fb5fb115cfc3`  
		Last Modified: Thu, 19 Feb 2026 00:29:06 GMT  
		Size: 618.3 KB (618289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ff2e5808ce5f57c3ed9120a75a5cb66e5de5cabbbfb8eebe8b5a40b9932c783`  
		Last Modified: Thu, 19 Feb 2026 00:29:05 GMT  
		Size: 41.1 KB (41116 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:2e0baad85133bc55b0c3dd05462a8a11c2277a7d7976d6ee65847fd67b314d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122296610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc0aa01d86d185c8d2de35b5536d73a050cca995878788f51e87417d834b9fcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 23:34:49 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 18 Feb 2026 23:34:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 18 Feb 2026 23:34:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 18 Feb 2026 23:34:55 GMT
ENV LANG=en_US.utf8
# Wed, 18 Feb 2026 23:34:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 18 Feb 2026 23:34:56 GMT
ENV PG_MAJOR=18
# Wed, 18 Feb 2026 23:34:56 GMT
ENV PG_VERSION=18.2
# Wed, 18 Feb 2026 23:34:56 GMT
ENV PG_SHA256=5245bd1b79700d55b8e0575be0325ef61e7bbef627e6a616e4cf36ad4687be36
# Wed, 18 Feb 2026 23:34:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 18 Feb 2026 23:38:38 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 		curl-dev 		liburing-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libcurl 		--with-liburing 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 18 Feb 2026 23:38:38 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 18 Feb 2026 23:38:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 18 Feb 2026 23:38:39 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 18 Feb 2026 23:38:39 GMT
VOLUME [/var/lib/postgresql]
# Wed, 18 Feb 2026 23:38:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 23:38:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 18 Feb 2026 23:38:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 Feb 2026 23:38:41 GMT
STOPSIGNAL SIGINT
# Wed, 18 Feb 2026 23:38:41 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 18 Feb 2026 23:38:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32e9b7742fe584659e12027c33c400a4177f291e191753d48596ef84ac6ec61`  
		Last Modified: Wed, 18 Feb 2026 23:39:16 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c587b197f828d0a7c74b82f2f928ac278b30f92c13e5af81025d5a49d694345`  
		Last Modified: Wed, 18 Feb 2026 23:39:16 GMT  
		Size: 897.4 KB (897419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46935794750250d4c2deff5705284e975fc3cb958496fa34e58c79c2db1962e`  
		Last Modified: Wed, 18 Feb 2026 23:39:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce16ecd413ac005463f0e1022932e833bb707a1a55d7819fd57b9d405d28d966`  
		Last Modified: Wed, 18 Feb 2026 23:39:18 GMT  
		Size: 117.6 MB (117647688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5954ecf262556f4d89d4152ed8bac0c407f4c26cddc89db3e49b5a29c8cbab41`  
		Last Modified: Wed, 18 Feb 2026 23:39:17 GMT  
		Size: 18.9 KB (18928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7c4bfae3520ca9f3143cdc048fe1481277c782a44a588450b71f913c1bde43`  
		Last Modified: Wed, 18 Feb 2026 23:39:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e876551e30f12580857b27bde4a899c9097fbbf835d0e6462e057baab0f2411`  
		Last Modified: Wed, 18 Feb 2026 23:39:17 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda9ba30bb0881ac3fc93f514d86d03a344042596a2a7c8b623d2b0d92d2ebe2`  
		Last Modified: Wed, 18 Feb 2026 23:39:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:38de7bf84c769ab3d46e00ee42660b8729e1e68474f985416b81b767c5af83d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.3 KB (659295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b77fab276d2f6a2d00f02d9218880857c8f355ea4e26b90ff6d94a98defa75`

```dockerfile
```

-	Layers:
	-	`sha256:a3de522d1e2ca385618a2aa0ceeed697cd1e33d277898e1dca4a9bf30a64b66e`  
		Last Modified: Wed, 18 Feb 2026 23:39:16 GMT  
		Size: 618.2 KB (618247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e691e980eb8a0eaf61f617097afdea7c72ff07646310df41084bb4000b5a2a5e`  
		Last Modified: Wed, 18 Feb 2026 23:39:16 GMT  
		Size: 41.0 KB (41048 bytes)  
		MIME: application/vnd.in-toto+json
