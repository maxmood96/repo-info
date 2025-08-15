## `postgres:14-alpine3.22`

```console
$ docker pull postgres@sha256:1d57730d43b38653b4689a6bc460499c5a9ec8952b71a1133559a23495fe85ae
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

### `postgres:14-alpine3.22` - linux; amd64

```console
$ docker pull postgres@sha256:f42bee6863fb4217b19b6b5bb80d01b78389190d2579133c378395b04ba291f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108261550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942fda8d333f0b977a0deaff993479168b6ce04327d255ac713dd87ca6d547f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:25:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_MAJOR=14
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_VERSION=14.19
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_SHA256=727e9e334bc1a31940df808259f69fe47a59f6d42174b22ae62d67fe7a01ad80
# Thu, 14 Aug 2025 16:25:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:25:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:25:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:25:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3279f7dbbba573fc1191af55409a8bca23d3fbe704262060a557d5518a687d`  
		Last Modified: Thu, 14 Aug 2025 18:23:57 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cfa9357baaf5f02c7a934cdf8f0180bf2ff81c95d425bc93e3c1a493d8d7af`  
		Last Modified: Thu, 14 Aug 2025 18:23:57 GMT  
		Size: 1.1 MB (1115582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bf25c5755deef58d1b4fb85f101dcb15fd4326877e5d6f5ce326db72c78d6e`  
		Last Modified: Thu, 14 Aug 2025 18:23:57 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2481d2b91b4c86930d7ece337d3718030786eeb4400347e8e0fcdd2624038eb0`  
		Last Modified: Thu, 14 Aug 2025 18:20:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613d66a1c19495a111520024685ac3dd5972d4f782a9b2b1bc2c789727342fa8`  
		Last Modified: Thu, 14 Aug 2025 20:09:18 GMT  
		Size: 103.3 MB (103329410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6e33f960ffade8e1277cc27489f7f97ee8f342ac2399997201453896c42e10`  
		Last Modified: Thu, 14 Aug 2025 18:23:57 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969585b9c845c0599fe0e9645fc45f8383ef14d98a9bb8159a0b5affec2d2678`  
		Last Modified: Thu, 14 Aug 2025 18:23:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a4c59c88d58413a5cbf5cbfb4527f5b33a2391673b50e37de749d7e6aeef26`  
		Last Modified: Thu, 14 Aug 2025 18:23:58 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572e0f290d7bed3aaa46f758e0475806999c1534574badb60144c9ef4ad20805`  
		Last Modified: Thu, 14 Aug 2025 18:23:58 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7444e777a728009ef8f80d7717486edb71dc64a81b7301587728044317a1ace6`  
		Last Modified: Thu, 14 Aug 2025 18:23:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:f7de23fb0a15f5640570c0cefe4a66a872261d5fa91022954da7b947ae07a2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.0 KB (640995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7f96cb52b921e504e43118c5c3f4abc20f7bf2f895acbb0fdb027087e3cb7e`

```dockerfile
```

-	Layers:
	-	`sha256:c0bceab6551c0790e502f1f46a3c7e091f7e34be16fd66c23294cb0a28fb9c66`  
		Last Modified: Thu, 14 Aug 2025 20:09:13 GMT  
		Size: 596.9 KB (596941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e68299295610940f34e3d37672486084e449a179503daaf5dabcf89d04e2725`  
		Last Modified: Thu, 14 Aug 2025 20:09:14 GMT  
		Size: 44.1 KB (44054 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; arm variant v6

```console
$ docker pull postgres@sha256:aa0d7c2dd61e20d803f3b5ca5867544094d28c1940d27d603f7d8554eadd6e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87877313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c652a60a470df933b3fad0be71808911af305246fc8de18677f536fd9daa4cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:25:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_MAJOR=14
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_VERSION=14.19
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_SHA256=727e9e334bc1a31940df808259f69fe47a59f6d42174b22ae62d67fe7a01ad80
# Thu, 14 Aug 2025 16:25:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:25:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:25:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:25:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079a1c87b1e4afd06564bb4788685a8121d0bc8ee1c65f7d29bae031097a898c`  
		Last Modified: Tue, 15 Jul 2025 21:59:03 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e018b614d5cbf1a0d8a1b23f428d5cbbbe192798ac0751d81172993ca1dbc93`  
		Last Modified: Tue, 15 Jul 2025 21:59:05 GMT  
		Size: 1.1 MB (1083508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7112f2e184ceefef9eeff37dd72d2f7909f3a223202968b7606e35232a4f6866`  
		Last Modified: Tue, 15 Jul 2025 22:16:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a57156ff7ae7b2ba746fdc40a1ad960d3dfd641362dd61bc3ad15b940144230`  
		Last Modified: Tue, 15 Jul 2025 22:16:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b013e4f98718586435fc752d8b9603789f77ed302b60f07352a029af0e5461a`  
		Last Modified: Thu, 14 Aug 2025 18:54:47 GMT  
		Size: 83.3 MB (83276020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01ee154330205d7ab59ed4ac6d57a7ad5874b2e8057a41ca46df69bf63b8d75`  
		Last Modified: Thu, 14 Aug 2025 18:54:31 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d22a7f4e0593de9904f1df44d03d7d0dcbfb9f74930744f436295317b72b9d`  
		Last Modified: Thu, 14 Aug 2025 18:54:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d50db1add0de7766922992ac6bedf152a5890d83b507acc6cfaeb07e56c116`  
		Last Modified: Thu, 14 Aug 2025 18:54:32 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eee5831e0c61f0ff94928add52336badbb9172a50b0446edcac531f319b58c`  
		Last Modified: Thu, 14 Aug 2025 18:54:32 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c05f323e044c947f22851efbe1edb59506e10d33e2fe178026584afdae6413`  
		Last Modified: Thu, 14 Aug 2025 18:54:32 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:edb22b981880058db1c09508b34d146e843504bbbd9f4b6af216f3d2d1ebdc21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 KB (44014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb6aa537c42617d8437ecc01d9ebbc3835df52fcbafc6888d24a422f1ed5922`

```dockerfile
```

-	Layers:
	-	`sha256:e3b643cd30572decc8d11063c1401b23e14fcb9b0096ca87431b3f2e7ee57ecc`  
		Last Modified: Thu, 14 Aug 2025 20:09:17 GMT  
		Size: 44.0 KB (44014 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; arm variant v7

```console
$ docker pull postgres@sha256:401853e11ff2f267e382c4f5ac27dee2195997a6c11ee4399d6b27699a60e6df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83180774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eddc7886c3bf439266a118e0c2d8ed195d4d0d0bf5ce71955501c9a65e0d9db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:25:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_MAJOR=14
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_VERSION=14.19
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_SHA256=727e9e334bc1a31940df808259f69fe47a59f6d42174b22ae62d67fe7a01ad80
# Thu, 14 Aug 2025 16:25:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:25:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:25:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:25:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d311585bee083aa9525f093872b6272f30fd05678140622cf8b253423af3dd`  
		Last Modified: Thu, 14 Aug 2025 18:50:36 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36a7751694a53e9a57d5356c38e15bbc8420fe128dc24f6b1156e5d65657148`  
		Last Modified: Thu, 14 Aug 2025 18:50:36 GMT  
		Size: 1.1 MB (1083514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbeb9513aa078b0eb8ce4bf6d95a7b7787beb9460a2af8d19a69c827e22729b`  
		Last Modified: Thu, 14 Aug 2025 20:10:32 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b458e6c32b35c52476942d750d16263a199db15b9a6e0c8c603fca6a5f8a2f1e`  
		Last Modified: Thu, 14 Aug 2025 20:10:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2e8eadbb9f95c745bdc10be5a8ebdd49aa487a165fa20ca6a0bacdee3b74c3`  
		Last Modified: Thu, 14 Aug 2025 21:08:00 GMT  
		Size: 78.9 MB (78861332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c139498a69e190e66cee8be68a8c64a5716403e1c23454ffefdf3d1b396273`  
		Last Modified: Thu, 14 Aug 2025 21:07:53 GMT  
		Size: 9.2 KB (9211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ba212a165a030301b20c10383cd572e3b3a361dc858d7b2130a9900fae9c46`  
		Last Modified: Thu, 14 Aug 2025 21:07:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022f3ebdb7a1a8c6428901794b5d55bb3b07d729510b780c5b5432c838cb558e`  
		Last Modified: Thu, 14 Aug 2025 21:07:53 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf984a3d05f39b15b3b2b5d1ebf66b560723ea5eab138681fafa2814cdec72b2`  
		Last Modified: Thu, 14 Aug 2025 21:07:53 GMT  
		Size: 5.9 KB (5932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffee36fee15de313cc3d586fdc099d075f1aac03c3584524ce96c5f9c50b846`  
		Last Modified: Thu, 14 Aug 2025 21:07:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:703e2a3244732070c4eef623186702856b7c2093182a996f6cc650a397ce4a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.2 KB (641206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f57f3aa24212df3ee610eedfb94541f08cb5af32950a2b237ac6333f8f67c6`

```dockerfile
```

-	Layers:
	-	`sha256:0cc332dd6694bf23f4c423bcc5406febd5feddddde529bd680251a720358b75d`  
		Last Modified: Thu, 14 Aug 2025 23:09:17 GMT  
		Size: 597.0 KB (596977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a07e46fab40fc427b31a0701a6508a36d6d3cfb38152b176f044680bb04a029`  
		Last Modified: Thu, 14 Aug 2025 23:09:18 GMT  
		Size: 44.2 KB (44229 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:c95adc3eff606507d8d8cbc0e6e909f3483bbbc8e11da045e0e879f273c92603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104195101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87912b808aebae66236e7c638b39e5ea1a4bdf9e24bea9f947b18819a1062b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:25:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_MAJOR=14
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_VERSION=14.19
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_SHA256=727e9e334bc1a31940df808259f69fe47a59f6d42174b22ae62d67fe7a01ad80
# Thu, 14 Aug 2025 16:25:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:25:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:25:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:25:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5c482840cf82de196008abc359484735770b13c9282408f1dca4d75164f7d5`  
		Last Modified: Thu, 14 Aug 2025 18:54:31 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e157a09d862e13d8d0e716ab97e9d5a2c94438123a639c16e3eab984125883e`  
		Last Modified: Thu, 14 Aug 2025 18:54:32 GMT  
		Size: 1.0 MB (1042499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beeac069caed963f46280d25489c8441ffe149df80d1667eb2108c8069089456`  
		Last Modified: Thu, 14 Aug 2025 19:09:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fac8997d1dffe2a81af36fccbdaf990b3b0a3dd0146bb736836b02cfc6164dd`  
		Last Modified: Thu, 14 Aug 2025 19:09:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cb7bf65f1325614ed6d3207cfd8c337b41beea6681904f1cd593f8e3c01320`  
		Last Modified: Thu, 14 Aug 2025 20:14:07 GMT  
		Size: 99.0 MB (99004973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352fc0ef0f00d5ce532d3341ef125e0dae0d1af150a1a30ea56bbc5d72c31a61`  
		Last Modified: Thu, 14 Aug 2025 19:24:33 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808cc7bc449b0a672b7287a234009481183f19ba10c7cf6900792159c2a0388f`  
		Last Modified: Thu, 14 Aug 2025 19:24:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0423a4a1fffe387aabc622e57ee9094bd0bafbf37ea803ce4e4d493da29abb`  
		Last Modified: Thu, 14 Aug 2025 19:24:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a6d865413b972ca4ae10072a150eca9e9fa0f56ccf6d481ecee67c86fd0144`  
		Last Modified: Thu, 14 Aug 2025 19:24:33 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa3473211101f90e1dfc036ac3121b81db2e11d6d42bfefc88bc2dc37ca69e2`  
		Last Modified: Thu, 14 Aug 2025 19:24:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:c7330974085f9ec4fd64d3cf0b7d6e9e071c0115cbbc18bd1f5aa3f65f4dbe7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.3 KB (641270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9492026aa355304739bd02fb8eea6113ec319d458510efc6ecb1b9924f4969`

```dockerfile
```

-	Layers:
	-	`sha256:a9ed6eb885469d4f56ed9682aee07ebe7e99d0bbe1354fd241a1e0e81e981e66`  
		Last Modified: Thu, 14 Aug 2025 20:09:46 GMT  
		Size: 597.0 KB (596997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c8eb448d53bd01f927ee86576c790b74eec77ef6d3da8c7ac9a4be64ee0505e`  
		Last Modified: Thu, 14 Aug 2025 20:09:47 GMT  
		Size: 44.3 KB (44273 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; 386

```console
$ docker pull postgres@sha256:44e29b1695ab3e110fb354567d1fe5545572d5399a9c560b6cf0a8246ad7fb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114485179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d66b7ce0687681ec2c8f77b4b62d9badf148f8a986b9d3ce9ca7dbc31a83491`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:25:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_MAJOR=14
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_VERSION=14.19
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_SHA256=727e9e334bc1a31940df808259f69fe47a59f6d42174b22ae62d67fe7a01ad80
# Thu, 14 Aug 2025 16:25:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:25:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:25:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:25:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa330b8928421d3194474b55918c4aa62911a2cfc94f583b5a8a1007d80cfee`  
		Last Modified: Thu, 14 Aug 2025 20:11:17 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc101c64486f7ac9ae027e5542e601fdfb313b314aebb56ba7d0cd8299a0e099`  
		Last Modified: Thu, 14 Aug 2025 20:11:09 GMT  
		Size: 1.1 MB (1091508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0178572e318c053c4b3339b8b63408fe08e71260b9f303148e79ed8fd887ab7`  
		Last Modified: Thu, 14 Aug 2025 20:11:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19947f6cc5d3035f6c922fa1d6047c79e044256ad948080adb59cec60717b9f8`  
		Last Modified: Thu, 14 Aug 2025 18:20:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c7e38f1cc2138b3fa0263555ce06a3ec6ddcc12be8e5d7c3bc7d3a84204305`  
		Last Modified: Thu, 14 Aug 2025 20:11:05 GMT  
		Size: 109.8 MB (109761789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ff4c99a9697ee94db0402bc203f358ce7542d174003c1ed0ea6627af12f242`  
		Last Modified: Thu, 14 Aug 2025 20:11:14 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f404917edcb8ee5a6cd0f73b294005e7d057e2ef9fb3b1ddd2becf07f86ec114`  
		Last Modified: Thu, 14 Aug 2025 20:11:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdcbb54f63b15d2d109465ed0a4141a28f96857248ba8de5a8b3ff24c396878`  
		Last Modified: Thu, 14 Aug 2025 20:11:16 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae00a6076b87a1edce80ac9c80404b463a3b8aad72f2cf3abc343fd047d599f`  
		Last Modified: Thu, 14 Aug 2025 20:11:16 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c5f8cb78ce9bb7853a937c12564f0e94625c6aafdb54a4fec3d9064871f5d8`  
		Last Modified: Thu, 14 Aug 2025 20:11:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:58a40571a550910ac4d3017e8547fde7fdddeca805c8cc15e7a91acc90b65599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.9 KB (640923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66b5a8a5695f8476cd16906ce2bbc39afe08199d7d75730ccf782213212ba31`

```dockerfile
```

-	Layers:
	-	`sha256:fa5659c6e08e725c75e8ac0a157492843d6831e10032ebbb787c5ad06bf3f705`  
		Last Modified: Thu, 14 Aug 2025 20:09:27 GMT  
		Size: 596.9 KB (596916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41d02e349b2fb22b94b706ecb744a6ae39c63f661fcf894b0a82f1164b129faa`  
		Last Modified: Thu, 14 Aug 2025 20:09:28 GMT  
		Size: 44.0 KB (44007 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; ppc64le

```console
$ docker pull postgres@sha256:ece6c22e33df7ccb9b3c80e411b0e92fa5675015ed1cee2231879a1c120687a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91918571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06381b90b95651d9c08c05f4dcc246e393b6b0bd812e87de73a293c609c15d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:25:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_MAJOR=14
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_VERSION=14.19
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_SHA256=727e9e334bc1a31940df808259f69fe47a59f6d42174b22ae62d67fe7a01ad80
# Thu, 14 Aug 2025 16:25:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:25:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:25:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:25:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5ee779caf31f6000861b5a827cc767777a7e523406271d594906edba47fb17`  
		Last Modified: Thu, 14 Aug 2025 19:04:33 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39e84474c9e8b921b5d1f181c420c8539aaff375b40eaaf2fb3eaa645a3f1c3`  
		Last Modified: Thu, 14 Aug 2025 19:04:34 GMT  
		Size: 1.0 MB (1032220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94ccd247fc85b417afdbafd53b06d2487171dda880c5aa0bd753a507fa6bf9`  
		Last Modified: Thu, 14 Aug 2025 19:28:31 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e2935a77d21eae07c28aac1c8fc1cacc4234ba4c89db92756482884273dd1a`  
		Last Modified: Thu, 14 Aug 2025 19:28:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075a8ce1795491f1b387270739384404aa8a65512e2eb7a9fb91c9d2d0a0d1d8`  
		Last Modified: Thu, 14 Aug 2025 19:51:53 GMT  
		Size: 87.1 MB (87142352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cd2fd23f67a8fa1e04a6463cd04a30ece9b14206120b698c5b1fe197703106`  
		Last Modified: Thu, 14 Aug 2025 19:51:48 GMT  
		Size: 9.2 KB (9210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038d1204517cd853ceebab282dcfd431ec2de76da3856508e0e30f8544f1ef40`  
		Last Modified: Thu, 14 Aug 2025 19:51:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed3d483eca0df488dd329b6df85f59aee6fafd99929d315591eee1829ce3c9f`  
		Last Modified: Thu, 14 Aug 2025 19:51:48 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ce252e51785d41882d64662438bbd55c3b4a5ce1e261960b69a798571cc03e`  
		Last Modified: Thu, 14 Aug 2025 19:51:49 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f0ba8c3c1cf772b7d932b28252da78ccd525a6e5d45f5c279d3d374a32c673`  
		Last Modified: Thu, 14 Aug 2025 19:51:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:aa3869321ac5d93f254d374900bd856434bdace89d180af343d35a1bb5d64488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.5 KB (637470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f0051ddf294ce8904893b00d7cbf7592523bf21192496488db4c5005836127`

```dockerfile
```

-	Layers:
	-	`sha256:710b182c73abe47362c0a9a873594904af9841cec0812d3b24c29b825d24176d`  
		Last Modified: Thu, 14 Aug 2025 20:09:33 GMT  
		Size: 593.4 KB (593362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4506b99e0c1e683017d66dc89770b0ed8019526486a370277273cc97a5ea9213`  
		Last Modified: Thu, 14 Aug 2025 20:09:34 GMT  
		Size: 44.1 KB (44108 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; riscv64

```console
$ docker pull postgres@sha256:4d138319b06f63918d1e580efae87c3c16108d9e39275e3e29f693f8eab63726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108122225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b344b4136ddb921aad5ed25812f07aa263ec7776c3390059bb5ea1c275680b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Jun 2025 18:27:47 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
CMD ["/bin/sh"]
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV LANG=en_US.utf8
# Fri, 06 Jun 2025 18:27:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_MAJOR=14
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_VERSION=14.18
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_SHA256=83ab29d6bfc3dc58b2ed3c664114fdfbeb6a0450c4b8d7fa69aee91e3ca14f8e
# Fri, 06 Jun 2025 18:27:47 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e4bf5c01f5fd5d5c2b6c78d1d884c92b6fce072812c2b64d8f250b5d9d572a`  
		Last Modified: Thu, 17 Jul 2025 04:54:24 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac990c2f318af1f8860277d49db61df409ca94944240be61871dfc66778de791`  
		Last Modified: Thu, 17 Jul 2025 04:54:24 GMT  
		Size: 1.1 MB (1085426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca4a60e5e84fee836f7f541710455c96ec0d3e445541a966a1d9f2df588a229`  
		Last Modified: Thu, 17 Jul 2025 08:31:18 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4e3883d3c5cb446972332da51687503a675e33ff0025674c2345ee1e0b2c2c`  
		Last Modified: Thu, 17 Jul 2025 08:31:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3eb15dcf61b6a984f3446dac30231cc5a247ebe70cea2a65cf062f3743b8f4`  
		Last Modified: Thu, 17 Jul 2025 11:55:24 GMT  
		Size: 103.5 MB (103507113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd97e58090f406dc597a432835dba57f9c6c36256f2bca5c5322dafe3137bf1`  
		Last Modified: Thu, 17 Jul 2025 11:55:12 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8aee7f277eff7a3ba45b5d62341fb95af544b0ef82ab45b22f6f8ba3df8d60`  
		Last Modified: Thu, 17 Jul 2025 11:55:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8c074cdf1a39fbe17f9df6ffc31510a85d1e40dcf3999affcad1f1ff6a6050`  
		Last Modified: Thu, 17 Jul 2025 11:55:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c08e4de3b45c0b3c8fad31f2a34a6766ca29b8c8ec875266f300373ec8e6b09`  
		Last Modified: Thu, 17 Jul 2025 11:55:12 GMT  
		Size: 5.9 KB (5933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e5713c5acfbbd3150a0c3e0f9f09edf342926c0560e3f523620b5c71a6669b`  
		Last Modified: Thu, 17 Jul 2025 11:55:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:0ec3109d6f36008af35cc57fb0cfa4139f25c1f62573ab6f892d68851534a77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.1 KB (639135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071627a012aacc399e75129b51131f80bfe68958b8fe8af9e0c847724fc7a0ef`

```dockerfile
```

-	Layers:
	-	`sha256:5b79aa62354c038cfe6e7916d6d9dc515e9a119904b7e7e815276be3996b3483`  
		Last Modified: Thu, 17 Jul 2025 14:08:03 GMT  
		Size: 595.0 KB (595020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e4af797487ad718ba77163920d4df478e9936e1ca9bb790185141adb8c4a582`  
		Last Modified: Thu, 17 Jul 2025 14:08:04 GMT  
		Size: 44.1 KB (44115 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.22` - linux; s390x

```console
$ docker pull postgres@sha256:8ac114f6c3aca6c06339e67fd0773ffa765fcc06cae80e84fe868060cda37c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116922067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3476f8cd3d15432171faf09ff725fcb3041def046925d786978ca9eeb33c6ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:25:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_MAJOR=14
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_VERSION=14.19
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_SHA256=727e9e334bc1a31940df808259f69fe47a59f6d42174b22ae62d67fe7a01ad80
# Thu, 14 Aug 2025 16:25:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:25:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:25:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:25:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d38346a6df0fbebdd4778252bbd39ccc90b12f4fad75fe53f1e3c72e66c3a5`  
		Last Modified: Thu, 14 Aug 2025 19:23:02 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0825e8e3a340fc788e6927d6d834d1119ad7c294a2a2b22dae232cf44b292106`  
		Last Modified: Thu, 14 Aug 2025 19:23:03 GMT  
		Size: 1.1 MB (1081138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c48dde862abb0bf8c1f4d6d3973dcd647cdc3c112341269fc042560074724b1`  
		Last Modified: Thu, 14 Aug 2025 21:07:27 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212811b83d554e8223a575869c18d4bdcde2acb8bef094cc619b59440c3584f2`  
		Last Modified: Thu, 14 Aug 2025 21:07:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70a74478ed670abfdaeed2be6eaccbf38872398e6d78654c243bdca2b02ea0d`  
		Last Modified: Thu, 14 Aug 2025 23:11:07 GMT  
		Size: 112.2 MB (112179087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70615dafffa14bffab399243eb7c16d5031e73a406587b0bde3a424be49b9cb9`  
		Last Modified: Thu, 14 Aug 2025 22:30:00 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724ade521ac2563809fcd34605255c58580bbcf87c4b10d3cdb7fced9e8b8577`  
		Last Modified: Thu, 14 Aug 2025 22:30:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee371cd0367a85369c98c9bc72e84415dc93231fc46b932b7931ad72b1213ee`  
		Last Modified: Thu, 14 Aug 2025 22:30:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12aa146689adc94f117ab3fa31dc16c214b544c142c91e9a630f561399a113d`  
		Last Modified: Thu, 14 Aug 2025 22:30:10 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34a9429b5bb6f10b48e437a8b04ab9b5c14d0bbc8770e5d972cbaea181fdd28`  
		Last Modified: Thu, 14 Aug 2025 22:30:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.22` - unknown; unknown

```console
$ docker pull postgres@sha256:c3c277f5cd763d9d66ed062ca181ef0b26ffa7cad90f79c61d0dec2539e22ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.0 KB (639045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e036b1a1088b34d1fadb14675c646ef1f8ef9aad537c6e5555f683a5750f3691`

```dockerfile
```

-	Layers:
	-	`sha256:6ad08bb0ce37ccae3bb5c493fc36b98bef4be99fdc2233496a92d88d6f110d9d`  
		Last Modified: Thu, 14 Aug 2025 23:09:31 GMT  
		Size: 595.0 KB (594990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07ad2b5c44e481c1f2023f43c79f78a7c072e02960a0c0c24a752f9db74547ce`  
		Last Modified: Thu, 14 Aug 2025 23:09:32 GMT  
		Size: 44.1 KB (44055 bytes)  
		MIME: application/vnd.in-toto+json
