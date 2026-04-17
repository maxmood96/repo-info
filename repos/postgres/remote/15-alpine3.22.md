## `postgres:15-alpine3.22`

```console
$ docker pull postgres@sha256:68e2ede1446ddd075b3b4b16c86e29a423dc0c22e85efa508cf893aa01190e3a
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

### `postgres:15-alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:f58aed41cefa0cef33c91af0628222e1eda8b9acc053513b6b710d5bda1d5d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108701559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da44a62077fc1f12afb1aff6c038e24f01bf8157723a717838523d5304cea6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:19 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 17 Apr 2026 00:19:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Apr 2026 00:19:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 00:19:21 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 17 Apr 2026 00:19:21 GMT
ENV LANG=en_US.utf8
# Fri, 17 Apr 2026 00:19:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 00:19:21 GMT
ENV PG_MAJOR=15
# Fri, 17 Apr 2026 00:19:21 GMT
ENV PG_VERSION=15.17
# Fri, 17 Apr 2026 00:19:21 GMT
ENV PG_SHA256=ae14f24c14727e0b2ded1c5553031666099bd1054db3ef44bfa6e2bd6d554a56
# Fri, 17 Apr 2026 00:19:21 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 17 Apr 2026 00:21:21 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 17 Apr 2026 00:21:21 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 17 Apr 2026 00:21:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 17 Apr 2026 00:21:21 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 17 Apr 2026 00:21:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 17 Apr 2026 00:21:21 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 17 Apr 2026 00:21:21 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:21:21 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 17 Apr 2026 00:21:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:21:21 GMT
STOPSIGNAL SIGINT
# Fri, 17 Apr 2026 00:21:21 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 17 Apr 2026 00:21:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516a1a5c300c183b56813d12ba8176f89f4dfb738bb673c6d59c56dcf6fafbe3`  
		Last Modified: Fri, 17 Apr 2026 00:21:35 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5fbadbaa6123f86927830fbb8021866fcab934e2247ec92132c9a355032c99`  
		Last Modified: Fri, 17 Apr 2026 00:21:35 GMT  
		Size: 917.4 KB (917425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c973c61e2a2afbe5fb8eda276ed173326247c57b6bcab361998150d94fda2d`  
		Last Modified: Fri, 17 Apr 2026 00:21:35 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940e6ba8a8302a94ca633f77be43627b3d34035d2d412f46d62058a739ace647`  
		Last Modified: Fri, 17 Apr 2026 00:21:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1274a8cece8aa40f994e143c392d0867284bce07df264a7762ee88af5c14827`  
		Last Modified: Fri, 17 Apr 2026 00:21:39 GMT  
		Size: 104.0 MB (103958911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82f5a9e013ce8733af54512b173adc5218fbd2604e7bc3023f5944a7a9af14f`  
		Last Modified: Fri, 17 Apr 2026 00:21:37 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b797dff0c279d3a15baf69fb8c6151cdf6e9f75bcb70f26ff68f816e84af6e`  
		Last Modified: Fri, 17 Apr 2026 00:21:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f495eade77a5e988b35f227ff6d82872bcf8231e4fbca51d98ff484f57ccf232`  
		Last Modified: Fri, 17 Apr 2026 00:21:37 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd48ecc96b3e21222a0d3ed0164c282269e0b90013ed74f6775f9f937828fead`  
		Last Modified: Fri, 17 Apr 2026 00:21:38 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752c3b5db845981e850a8605ee3c83a3bd5388f21f64baad523c4f73f9ccde15`  
		Last Modified: Fri, 17 Apr 2026 00:21:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:933d58bbb897cf1d18123e2788d37ef7309a6081e5002ffc0edf7cfc77951148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.1 KB (640083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5858eb1e697a32fb13c7636d2bc3e479a6f102d820bd3b5152e9cf7a7377c71b`

```dockerfile
```

-	Layers:
	-	`sha256:e8fb1ffd67baa8bc06446462599833f53cc22622cedb21f4c6af0350e5c7ac29`  
		Last Modified: Fri, 17 Apr 2026 00:21:35 GMT  
		Size: 596.3 KB (596315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:271d09a82b4509dfc649c5b2f1db1280dd4166ef86d8636b07f7a6d786d527d9`  
		Last Modified: Fri, 17 Apr 2026 00:21:35 GMT  
		Size: 43.8 KB (43768 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:57bd4a1c92f8179bbc429e69f1effca0d54e51e0bfd7ddea9212a93d3ad5819f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88311534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ae970eab380eaaf6a22258d3b5254b82a05e2bad5dc0dba3e9fb23a015c154`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:25:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 17 Apr 2026 00:25:18 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Apr 2026 00:25:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 00:25:18 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 17 Apr 2026 00:25:18 GMT
ENV LANG=en_US.utf8
# Fri, 17 Apr 2026 00:25:18 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 00:25:18 GMT
ENV PG_MAJOR=15
# Fri, 17 Apr 2026 00:25:18 GMT
ENV PG_VERSION=15.17
# Fri, 17 Apr 2026 00:25:18 GMT
ENV PG_SHA256=ae14f24c14727e0b2ded1c5553031666099bd1054db3ef44bfa6e2bd6d554a56
# Fri, 17 Apr 2026 00:25:18 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 17 Apr 2026 00:28:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 17 Apr 2026 00:28:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 17 Apr 2026 00:28:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 17 Apr 2026 00:28:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 17 Apr 2026 00:28:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 17 Apr 2026 00:28:01 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 17 Apr 2026 00:28:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:28:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 17 Apr 2026 00:28:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:28:02 GMT
STOPSIGNAL SIGINT
# Fri, 17 Apr 2026 00:28:02 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 17 Apr 2026 00:28:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4d75008e4a5d9208b5bdc733fee121cac58ff75ff8a7eb7db9094fbed4a6f8`  
		Last Modified: Fri, 17 Apr 2026 00:28:12 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9c698c190e70fe4ce8c67a7c3702ca65bbf62a98e602d5ea53e46a94d80a68`  
		Last Modified: Fri, 17 Apr 2026 00:28:12 GMT  
		Size: 885.1 KB (885149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8aad1e6294f07ae92f99874cc6db73d387e723af17662fed39f4813c6e3da4a`  
		Last Modified: Fri, 17 Apr 2026 00:28:12 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40b03c363955d5651ab46b728190ac3811a456cf124db3e318760c42f2c8943`  
		Last Modified: Fri, 17 Apr 2026 00:28:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0902ac4ae86599e0b0a50e60dfe9e0395cb9c926d49ec38559dceda356648806`  
		Last Modified: Fri, 17 Apr 2026 00:28:15 GMT  
		Size: 83.9 MB (83901979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec3dc9937608a08015ac1ce9824903b6cec5d888aff82f5f3f8da084e060a3d`  
		Last Modified: Fri, 17 Apr 2026 00:28:13 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f80bd7d847f2173b6aa2c64f3fcf6cf6b4030d6146a49fba44452522aef933`  
		Last Modified: Fri, 17 Apr 2026 00:28:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9f605475f4a2cb72f39640b9b24bfd60116409019545cbe4bfade096ed3e80`  
		Last Modified: Fri, 17 Apr 2026 00:28:13 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f52dcf58293ce64f31395b6c250a1b260d3facdcfe1c2205e426053aa61c25`  
		Last Modified: Fri, 17 Apr 2026 00:28:14 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e319611132d3dd252c12abc0d335fbd92c5ce5d127f98d25beab793770dc079`  
		Last Modified: Fri, 17 Apr 2026 00:28:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:d54772f4b238d2fdf53d4187c75fef6048cc4248e73a1e1c6a8678dbb9aba3c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 KB (43715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9722475789b50555654dfdd89146d28873c65fe09a469d809109384f813dfec8`

```dockerfile
```

-	Layers:
	-	`sha256:0b3e6cb69bc8e7370906a6cb97e86cc9bacfe50a7d97ec3d6df64cfb1eeedd55`  
		Last Modified: Fri, 17 Apr 2026 00:28:12 GMT  
		Size: 43.7 KB (43715 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:26f0da051ea8f5199fff792825be89db29243acd12b46e913db0dc71ee09d353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83597699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da42fe0258cd0c88445bf81f612e8c247fa1be708dae881becf3eca29a47c72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:25:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 17 Apr 2026 00:25:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Apr 2026 00:25:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 00:25:21 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 17 Apr 2026 00:25:21 GMT
ENV LANG=en_US.utf8
# Fri, 17 Apr 2026 00:25:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 00:25:21 GMT
ENV PG_MAJOR=15
# Fri, 17 Apr 2026 00:25:21 GMT
ENV PG_VERSION=15.17
# Fri, 17 Apr 2026 00:25:21 GMT
ENV PG_SHA256=ae14f24c14727e0b2ded1c5553031666099bd1054db3ef44bfa6e2bd6d554a56
# Fri, 17 Apr 2026 00:25:21 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 17 Apr 2026 00:28:00 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 17 Apr 2026 00:28:00 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 17 Apr 2026 00:28:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 17 Apr 2026 00:28:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 17 Apr 2026 00:28:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 17 Apr 2026 00:28:00 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 17 Apr 2026 00:28:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:28:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 17 Apr 2026 00:28:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:28:00 GMT
STOPSIGNAL SIGINT
# Fri, 17 Apr 2026 00:28:00 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 17 Apr 2026 00:28:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30bb6fd58ee0cb79b57b0b59b982ad3e5eb2f9feb113c86472cb655dffe085d`  
		Last Modified: Fri, 17 Apr 2026 00:28:11 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09a0d986c0537f865aba3eda4901f6c7a9ffe8b4f87743807461b7818098081`  
		Last Modified: Fri, 17 Apr 2026 00:28:11 GMT  
		Size: 885.2 KB (885152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfecd363a8406a68ab870336db8e57ba6564ace13d9ef7cadad45b679879050`  
		Last Modified: Fri, 17 Apr 2026 00:28:11 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53f0ef7f8ddd4c42d8e3adaf0e728dafedc61dffabede512f86d4df0de359d1`  
		Last Modified: Fri, 17 Apr 2026 00:28:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfb3cd108226205c6e24f0058d530be1d3542e1ea9e1a9bfad9a3926ae6ed90`  
		Last Modified: Fri, 17 Apr 2026 00:28:15 GMT  
		Size: 79.5 MB (79469687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7603cee44c0d7b8f9054ad94d67cdf403999e451fb42c48d9a96c88698e3d3`  
		Last Modified: Fri, 17 Apr 2026 00:28:13 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365e94b9be5c9088e10514fb5d4c45fae5c9fbbeee4dc0a631df15e35d305e08`  
		Last Modified: Fri, 17 Apr 2026 00:28:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344290b361720c5d3e58e55895b186aedb89a3cee72cf121fd969c8798ed7b8d`  
		Last Modified: Fri, 17 Apr 2026 00:28:13 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a833bff9f1f83fba3762445c378fe6b61bf5156e09a08266ceed69faa8ab55e`  
		Last Modified: Fri, 17 Apr 2026 00:28:14 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b076c3049bb20b44549f3ae3dabe95d1db92ff63cbba067ad3cca33a853182`  
		Last Modified: Fri, 17 Apr 2026 00:28:14 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:7b9a2345e30d0fc2c0a599a2814a54869a2308405f2933f57a4faeb669b51992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.3 KB (640265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3be2be8fa7ce52c7f3cb6fa04b41ced129e5772097dccf3e50b734e98b32723`

```dockerfile
```

-	Layers:
	-	`sha256:d3f4a90df7170077b9b207e29532fea7d3f77a1572f962934a5e29a11df088aa`  
		Last Modified: Fri, 17 Apr 2026 00:28:12 GMT  
		Size: 596.3 KB (596335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77bfa33d40b90aef5079400f02f68ca02029b187511eabd15473efc69af3eaa0`  
		Last Modified: Fri, 17 Apr 2026 00:28:11 GMT  
		Size: 43.9 KB (43930 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:123c8db7cc6f00e22f81daf3b1f9265b2c20fd583a95946fd7e039015e11ae21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104679147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf629efd636a4b3cb5dbf538779c1bf02990300db6bea21786efbd50b2baac1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:20:02 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 17 Apr 2026 00:20:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 17 Apr 2026 00:20:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 17 Apr 2026 00:20:05 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 17 Apr 2026 00:20:05 GMT
ENV LANG=en_US.utf8
# Fri, 17 Apr 2026 00:20:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 00:20:05 GMT
ENV PG_MAJOR=15
# Fri, 17 Apr 2026 00:20:05 GMT
ENV PG_VERSION=15.17
# Fri, 17 Apr 2026 00:20:05 GMT
ENV PG_SHA256=ae14f24c14727e0b2ded1c5553031666099bd1054db3ef44bfa6e2bd6d554a56
# Fri, 17 Apr 2026 00:20:05 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 17 Apr 2026 00:22:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 17 Apr 2026 00:22:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 17 Apr 2026 00:22:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 17 Apr 2026 00:22:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 17 Apr 2026 00:22:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 17 Apr 2026 00:22:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 17 Apr 2026 00:22:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:22:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 17 Apr 2026 00:22:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:22:30 GMT
STOPSIGNAL SIGINT
# Fri, 17 Apr 2026 00:22:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 17 Apr 2026 00:22:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79190a2432750eca69e95eb3d8027257861f59516d6acc83a49a0ed6251a8a43`  
		Last Modified: Fri, 17 Apr 2026 00:22:44 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd3a084289bcfc44a2ce4bedfaad650c0a6d5e7e80e37b06a25134302ffb98c`  
		Last Modified: Fri, 17 Apr 2026 00:22:45 GMT  
		Size: 873.1 KB (873123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0f6b8b00dd1ba013bc368ba4145b05e4ab9198e475f09d2a1af9f6ea576a50`  
		Last Modified: Fri, 17 Apr 2026 00:22:44 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b44024a70654fa818c28808ce7c0a2885557cca062c0b659cc8ef4e97ff2ca`  
		Last Modified: Fri, 17 Apr 2026 00:22:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cee1cc0c22bf07a1a4c3785834ab275313e99630a751de11a8c1acf5cb04b7`  
		Last Modified: Fri, 17 Apr 2026 00:22:48 GMT  
		Size: 99.6 MB (99647088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807d3b7e48895209d1799e10b800a5c85dee38230ce99ca16be752b62d7c9123`  
		Last Modified: Fri, 17 Apr 2026 00:22:46 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387db3d901c60e942315c4fdec9cc2b01c42b311e816dfd599b4b3617de7cff0`  
		Last Modified: Fri, 17 Apr 2026 00:22:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041048346de6984f2f8aba67ee1214dcc25874e1d3de536c47958e492ffdeaf7`  
		Last Modified: Fri, 17 Apr 2026 00:22:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20524f50c4928da1894f4fd6c19bcb0f96c2771dfd84dcadd6de3b82b5ee0270`  
		Last Modified: Fri, 17 Apr 2026 00:22:47 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde3fef2681e4c89bd481a1eaff02a59ecf0f19416de9ac50ee038214f0a875f`  
		Last Modified: Fri, 17 Apr 2026 00:22:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:a644cba8d0b5c610c20f617a991c45ca3902ed5ec541542606282a9d85514295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.3 KB (640309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:effc4000b533e8fd6b9affcd1ec979961ea397b0576107c115f123730bcdf80a`

```dockerfile
```

-	Layers:
	-	`sha256:35754984452be3ca7e0cb52fb35a4786f24a7ae066738b18663a2e23fcd1895c`  
		Last Modified: Fri, 17 Apr 2026 00:22:45 GMT  
		Size: 596.3 KB (596347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef223f530bd2443f5316a157404360bbd85ca53b2aa8b4cb9ea62e39270e1788`  
		Last Modified: Fri, 17 Apr 2026 00:22:44 GMT  
		Size: 44.0 KB (43962 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:75bee6b387c56c2101a20a2a9dac6328f07fcda886b209830bb95e61d5ed9f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (114950271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd0c1f2b8b9d47e9c12ef944ba39acebcec1201d17d0a6ab05d6f3974ec2e2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Thu, 26 Feb 2026 19:16:26 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:16:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:16:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:22:29 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 26 Feb 2026 19:22:29 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:22:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:22:29 GMT
ENV PG_MAJOR=15
# Thu, 26 Feb 2026 19:22:29 GMT
ENV PG_VERSION=15.17
# Thu, 26 Feb 2026 19:22:29 GMT
ENV PG_SHA256=ae14f24c14727e0b2ded1c5553031666099bd1054db3ef44bfa6e2bd6d554a56
# Thu, 26 Feb 2026 19:22:29 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 26 Feb 2026 19:24:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:24:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:24:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:24:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:24:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:24:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:24:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:24:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:24:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:24:41 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:24:41 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:24:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f900c73cf7d491355f8ccb851c8ca2a2cd6bf5a4528e310a1d428dd0852859ef`  
		Last Modified: Thu, 26 Feb 2026 19:19:31 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaafe8751749cbb48fe9aba2611892ad7eec97371aee19e5458f87b867dc3a5`  
		Last Modified: Thu, 26 Feb 2026 19:19:31 GMT  
		Size: 890.6 KB (890637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7072ac653b1fabd040f91f7a89f8aa3d3a0cd08e1b7c0ac63a94a62dec0de69c`  
		Last Modified: Thu, 26 Feb 2026 19:24:56 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d324075d4825a4a395138fda6a14f09ac09be329122a6f45808e9c425ba491a1`  
		Last Modified: Thu, 26 Feb 2026 19:24:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9152c609e90729c1f0103264774054ec39150caf3d6392362219997ca515d008`  
		Last Modified: Thu, 26 Feb 2026 19:24:59 GMT  
		Size: 110.4 MB (110421868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be986ca1234de82079ef11ed1322b1761425db3a131d9c13d582395186b602ac`  
		Last Modified: Thu, 26 Feb 2026 19:24:56 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a34799ad39c091849969c0037d8e84c3e4473bec582997d4c44466ca7f3ddd`  
		Last Modified: Thu, 26 Feb 2026 19:24:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3223b9566b670f3f660aadd81676d0b2994266676a77890c37d350311bf7a5c0`  
		Last Modified: Thu, 26 Feb 2026 19:24:58 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797da6860f74f23ed259052bdc42b4a4ec384b5585b0a9d0fc6b2c6d2453e133`  
		Last Modified: Thu, 26 Feb 2026 19:24:58 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706292180dc4a4aefb77421810e7eb9fbed9354afed0a1d578e2482106d060f4`  
		Last Modified: Thu, 26 Feb 2026 19:24:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:c830e960539a50cd348595ece1b4522ccc213817078f15a81110b317548537b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.0 KB (640030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f137d329e237a57d366401cfea6b393010a0f1285dbb4ec120ddf59fe9eddd`

```dockerfile
```

-	Layers:
	-	`sha256:3f0df10c00dbbebf585f45dbc904f9c20d0f9ca51c515e693f6c1e9d5c488d09`  
		Last Modified: Thu, 26 Feb 2026 19:24:56 GMT  
		Size: 596.3 KB (596300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cd9894b32c489f244619a4bbdeed72b0abb28b6668c2104c67a1386948915d8`  
		Last Modified: Thu, 26 Feb 2026 19:24:56 GMT  
		Size: 43.7 KB (43730 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:23006ae372faf95178cdf06bd5977180d2f5e5dc3a8db5b1ea3cda703beca0fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92461334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e384fa4ebc5a624778396835485396a0817dd579cd24a7314985fb98d236c87`
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
# Fri, 17 Apr 2026 01:01:39 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 17 Apr 2026 01:01:39 GMT
ENV LANG=en_US.utf8
# Fri, 17 Apr 2026 01:01:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 01:01:41 GMT
ENV PG_MAJOR=15
# Fri, 17 Apr 2026 01:01:41 GMT
ENV PG_VERSION=15.17
# Fri, 17 Apr 2026 01:01:41 GMT
ENV PG_SHA256=ae14f24c14727e0b2ded1c5553031666099bd1054db3ef44bfa6e2bd6d554a56
# Fri, 17 Apr 2026 01:01:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 17 Apr 2026 01:05:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 17 Apr 2026 01:05:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 17 Apr 2026 01:05:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 17 Apr 2026 01:05:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 17 Apr 2026 01:05:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 17 Apr 2026 01:05:33 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 17 Apr 2026 01:05:34 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:05:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 17 Apr 2026 01:05:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:05:35 GMT
STOPSIGNAL SIGINT
# Fri, 17 Apr 2026 01:05:35 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 17 Apr 2026 01:05:35 GMT
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
	-	`sha256:1c70dfbaf97c3011265a74c613fd16f2b58f99917b21da4f87f1a93ff3b34dfa`  
		Last Modified: Fri, 17 Apr 2026 01:05:48 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ee1fb225d778c596655a48908ccf2b01fb7422624a9d500fa81bcdff64aa0d`  
		Last Modified: Fri, 17 Apr 2026 01:05:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5681ecd432e4f194b1f33e8720b9562ea0b650c3a4e2488fd482183c6830212`  
		Last Modified: Fri, 17 Apr 2026 01:06:07 GMT  
		Size: 87.8 MB (87829329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5834f4d3ee2f6da21ef1d88265246b78a4dd9a13616c6c5b484bfd95b8868d38`  
		Last Modified: Fri, 17 Apr 2026 01:06:04 GMT  
		Size: 9.5 KB (9456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14aa31c630b8aaa8de83c5e22969a7a6ac5495a0c65e14491d3f99d63d7bafa2`  
		Last Modified: Fri, 17 Apr 2026 01:06:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9ac5868116fc0c9decb7675c6a35cb9a86d1b6ba428b3a170ca13b1131085a`  
		Last Modified: Fri, 17 Apr 2026 01:06:04 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43decd2f044fdc8819773983c8812dbc9ab90cfd08cdc3745a96dd0d338ad514`  
		Last Modified: Fri, 17 Apr 2026 01:06:06 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6f5f5b2031f48c0a44a38dda06622603aa9906f3f5b2003dab3649492b3aed`  
		Last Modified: Fri, 17 Apr 2026 01:06:06 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:b1566026b8eea6da39dd8b0ade98cb72989a4085f6f86ece4a1bb5e65d4c8b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.5 KB (636534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d7de3356d6df014d7692e6698cb7721da51389c4983c73b9acbc2b78cf06c5`

```dockerfile
```

-	Layers:
	-	`sha256:d9901b282d3a2ab81ca254c16db83c9c7eded7a69d8a6051fd49b978c26c433b`  
		Last Modified: Fri, 17 Apr 2026 01:06:04 GMT  
		Size: 592.7 KB (592724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f22726451280f9b2caae7a10405bda316852556ae9c8f92ff35f35e08034d47c`  
		Last Modified: Fri, 17 Apr 2026 01:06:04 GMT  
		Size: 43.8 KB (43810 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:121b4dc1b708281b67188f64d0b617fc0ff6b1121bef1941763bfd0601eb4d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108635021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e89e464b59dbecf077b96dab777d56a4beab074651cf96932d031b21d8649f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Fri, 13 Feb 2026 00:03:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 13 Feb 2026 00:03:22 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Feb 2026 00:03:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Feb 2026 08:02:34 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 13 Feb 2026 08:02:34 GMT
ENV LANG=en_US.utf8
# Sat, 28 Feb 2026 10:59:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 28 Feb 2026 10:59:41 GMT
ENV PG_MAJOR=15
# Sat, 28 Feb 2026 10:59:41 GMT
ENV PG_VERSION=15.17
# Sat, 28 Feb 2026 10:59:41 GMT
ENV PG_SHA256=ae14f24c14727e0b2ded1c5553031666099bd1054db3ef44bfa6e2bd6d554a56
# Sat, 28 Feb 2026 10:59:41 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Sat, 28 Feb 2026 13:37:42 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Sat, 28 Feb 2026 13:37:43 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 28 Feb 2026 13:37:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 28 Feb 2026 13:37:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 28 Feb 2026 13:37:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sat, 28 Feb 2026 13:37:44 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 28 Feb 2026 13:37:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 13:37:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 28 Feb 2026 13:37:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 13:37:45 GMT
STOPSIGNAL SIGINT
# Sat, 28 Feb 2026 13:37:45 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 28 Feb 2026 13:37:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9a8d29c18a7aa35e1e673e585403324e4011c659e3a9af9631eeef53eb1abe`  
		Last Modified: Fri, 13 Feb 2026 00:55:28 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f6ced6daa9dca5801962fab9724b150e63d0b23f3667a8a57104fdc08d51d`  
		Last Modified: Fri, 13 Feb 2026 00:55:28 GMT  
		Size: 866.6 KB (866630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fefaa019570f036a479949adc1cff90d83d62dfcccda924ecbc9fb276d79751`  
		Last Modified: Fri, 13 Feb 2026 08:54:08 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a21a3b98c9b6bafb53cc153f92fb4167f502f246a409bab23715b2cfca06be`  
		Last Modified: Sat, 28 Feb 2026 11:51:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7a08211201b2792c6da6491c67f7c0b60d2aaf6affe17768497d825758c1be`  
		Last Modified: Sat, 28 Feb 2026 13:40:43 GMT  
		Size: 104.2 MB (104233919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa65748c7c99e33981d9e49366d26c1a81c773734eadce646d7af0e554cb820a`  
		Last Modified: Sat, 28 Feb 2026 13:40:28 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb1350e509c0580f62fa96d9da93d77c8420ecfaf1bac572c03de13755375dc`  
		Last Modified: Sat, 28 Feb 2026 13:40:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4222b85b91f25baa4eaf654f6b9b36622f6bf7aacad98f4d3b93e61deebaac`  
		Last Modified: Sat, 28 Feb 2026 13:40:28 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b9e2ac739b496d95f5c41cc08aa01ec8c6b0c283d0b793a4d46bcd57fa6ac3`  
		Last Modified: Sat, 28 Feb 2026 13:40:29 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aada459050ae76a1982c75406c3dfc55a5edccc373609ff9fec1a3894e778d0`  
		Last Modified: Sat, 28 Feb 2026 13:40:29 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:6570d1f4e7cc23d6d68bcea14d633ab3376facdc4a0582ef632a0603f0595f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.2 KB (638198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f850561960c78330fbb0485470b856f1c28696b2c28f60a364b2102b093709e`

```dockerfile
```

-	Layers:
	-	`sha256:eb8b560be1f61c7f76616c2dc6701a0556c689a84ff400f1f5f6fb85790f70c5`  
		Last Modified: Sat, 28 Feb 2026 13:40:28 GMT  
		Size: 594.4 KB (594382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4a36abeb1792f22a44b8f0b9fa94715207e9df1b8f186c4b3d9fae414cb956b`  
		Last Modified: Sat, 28 Feb 2026 13:40:28 GMT  
		Size: 43.8 KB (43816 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:cbe0eed9e288662321220baafbb195894eaf8eb1ebdde87ea57ed2b0d5470931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 MB (117403699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5cc7f8cede2e66340b73dd3a9170a2d7bc9f172a108652113ebc5d16f12761`
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
# Fri, 17 Apr 2026 00:32:21 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 17 Apr 2026 00:32:21 GMT
ENV LANG=en_US.utf8
# Fri, 17 Apr 2026 00:32:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 00:32:21 GMT
ENV PG_MAJOR=15
# Fri, 17 Apr 2026 00:32:21 GMT
ENV PG_VERSION=15.17
# Fri, 17 Apr 2026 00:32:21 GMT
ENV PG_SHA256=ae14f24c14727e0b2ded1c5553031666099bd1054db3ef44bfa6e2bd6d554a56
# Fri, 17 Apr 2026 00:32:21 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 17 Apr 2026 00:36:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 17 Apr 2026 00:36:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 17 Apr 2026 00:36:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 17 Apr 2026 00:36:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 17 Apr 2026 00:36:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 17 Apr 2026 00:36:41 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 17 Apr 2026 00:36:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:36:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 17 Apr 2026 00:36:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:36:41 GMT
STOPSIGNAL SIGINT
# Fri, 17 Apr 2026 00:36:41 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 17 Apr 2026 00:36:41 GMT
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
	-	`sha256:bb76a42752ed59f6675aba6aa5579902187844809fb4606a80d654b0537323c9`  
		Last Modified: Fri, 17 Apr 2026 00:37:05 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bade5ff2e60ad4f14c995b84ea20bac0cbe1045346ff1378fd0c5d479e24d76`  
		Last Modified: Fri, 17 Apr 2026 00:37:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ebfa8544070fd42477f6b11962f41369a19219a010aec8f4ccb74bfa402b4d`  
		Last Modified: Fri, 17 Apr 2026 00:37:08 GMT  
		Size: 112.8 MB (112838550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3428f262dcbdd608fbd693d6d1489c65509082b72de46dfa8ae8bb6d6824609e`  
		Last Modified: Fri, 17 Apr 2026 00:37:06 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329a34f1407f135099d3d5055f90b198aecd4ff5e30b5f8460dec6e5c37206d2`  
		Last Modified: Fri, 17 Apr 2026 00:37:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3f1462079cb305c7028923f243c87b516cf00bcc7c34a44f7190c5ac4757ea`  
		Last Modified: Fri, 17 Apr 2026 00:37:06 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a059ad311b9c8d5a4aff67c3380dac0f49b7754a13bcf422b5771cd28a06ba`  
		Last Modified: Fri, 17 Apr 2026 00:37:07 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135456b89cf9537a7ee799dcd1d1c8c1adcce658c1e383285401b95e6cee7fb2`  
		Last Modified: Fri, 17 Apr 2026 00:37:07 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:8dc1ee1c2a7f5cf76dfba56d77d7dfffaecdcda1b5fc01215854fc22f92d9f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.1 KB (638132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba688587ee2b3ede50d2ffef7d2050a34776a9ea6bd1799c9c4fe6102c7e58f`

```dockerfile
```

-	Layers:
	-	`sha256:25dba45ba66270002493aab97b2ddb018b0a166dad4d5caf3bc823b82a029a7e`  
		Last Modified: Fri, 17 Apr 2026 00:37:05 GMT  
		Size: 594.4 KB (594364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3a3e91ad9248c1fc101fddea5dc04eb65269a11c6b14c1c346d2a12a63e135d`  
		Last Modified: Fri, 17 Apr 2026 00:37:05 GMT  
		Size: 43.8 KB (43768 bytes)  
		MIME: application/vnd.in-toto+json
