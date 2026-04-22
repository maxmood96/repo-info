## `postgres:15-alpine`

```console
$ docker pull postgres@sha256:eb72e44fdca6270e882be90645eaf7af032f55a45dbf096ba4dd9d08195b08e3
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

### `postgres:15-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:b4a5f2de972016bd62ded6206c10face6ed16a469ef276c569dd130cb2f07f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109158210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1dd58d6cec8e67cb85b2c8fd200fa870697269c5024e59627095326a8254ae2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:08:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:08:10 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:08:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:08:10 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 21 Apr 2026 23:08:10 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:08:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:08:11 GMT
ENV PG_MAJOR=15
# Tue, 21 Apr 2026 23:08:11 GMT
ENV PG_VERSION=15.17
# Tue, 21 Apr 2026 23:08:11 GMT
ENV PG_SHA256=ae14f24c14727e0b2ded1c5553031666099bd1054db3ef44bfa6e2bd6d554a56
# Tue, 21 Apr 2026 23:08:11 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:10:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:10:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:10:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:10:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Apr 2026 23:10:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 21 Apr 2026 23:10:14 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:10:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:10:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:10:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:10:14 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:10:14 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:10:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae1993563ec67f988a5501162b347d09a1679342cb183d7467ef420aee6e6cc`  
		Last Modified: Tue, 21 Apr 2026 23:10:29 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013d59842ad1bc1e18c6f8c5182756915df7e1226b5971b82052246f368db2c4`  
		Last Modified: Tue, 21 Apr 2026 23:10:29 GMT  
		Size: 919.1 KB (919055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf7646f4ff5655f621e9bf760783a9b4f89c016ee494ea40a40fc8a96a0a146`  
		Last Modified: Tue, 21 Apr 2026 23:10:29 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459be1018dcb7bbe85b04bbab33af716a0694bc21d324ea663280a7b026fd32c`  
		Last Modified: Tue, 21 Apr 2026 23:10:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697a7e77ac2e14119411f4d54374d81585a34a695a82e1163052ee1e6bac6632`  
		Last Modified: Tue, 21 Apr 2026 23:10:33 GMT  
		Size: 104.4 MB (104357683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0bf5bcb56f5d77f08ba5b5c26ac3250ee7d4b44d9a6c20f828c35a885823b9`  
		Last Modified: Tue, 21 Apr 2026 23:10:31 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a63010ee4dedc7c774c9cd8834e62e27eba3ac4caa21a63192bf21bf14c3ce`  
		Last Modified: Tue, 21 Apr 2026 23:10:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5206f96f8a8d318aa75bc1488b66f99a081a63e259a80c065b7414dc0d0d49e2`  
		Last Modified: Tue, 21 Apr 2026 23:10:31 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523b9d9d62548b93e0d6e5dc8b69f9e8c15d7ed1a44692f532b40dea9f916128`  
		Last Modified: Tue, 21 Apr 2026 23:10:32 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2769f58dd89f2443adc8a98bfb2ca0a6cbe8d1ed6ee8da9c3a328585a38fb4`  
		Last Modified: Tue, 21 Apr 2026 23:10:32 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:59e4302bc7fff83d1bfe68a76a0fd3520773923edd0fb133c5c946fa3dc8fdee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.5 KB (642498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e05d6d1a8af8785ce7ba2bc5e653e7608a6120d3abc239c0085bc51aec806f`

```dockerfile
```

-	Layers:
	-	`sha256:28e69896d9dab36231c199c073c55000b3d6ce49592db18119177fa57afc6ae5`  
		Last Modified: Tue, 21 Apr 2026 23:10:29 GMT  
		Size: 598.1 KB (598108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b6ad35bb4369cec173e0a23ef2b263fc512cae8ae191d1500165f86e7d6c683`  
		Last Modified: Tue, 21 Apr 2026 23:10:29 GMT  
		Size: 44.4 KB (44390 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:5637e71a9cde28478d76505ee7ab170a140fdd032fc8632dc14c6c52aa2d9f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88649756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8666c3d8b08901a9b8637b8b297b833704ce05b2fe6071a90c7f0d380732ba69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:16:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:16:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:16:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:16:19 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 21 Apr 2026 23:16:19 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:16:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:16:19 GMT
ENV PG_MAJOR=15
# Tue, 21 Apr 2026 23:16:19 GMT
ENV PG_VERSION=15.17
# Tue, 21 Apr 2026 23:16:19 GMT
ENV PG_SHA256=ae14f24c14727e0b2ded1c5553031666099bd1054db3ef44bfa6e2bd6d554a56
# Tue, 21 Apr 2026 23:16:19 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:19:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:19:07 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:19:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:19:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Apr 2026 23:19:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 21 Apr 2026 23:19:07 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:19:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:19:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:19:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:19:07 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:19:07 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:19:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6efde4c69c8bad369681a5c4976b032e9a264053fe67cca506ec84e8678cc8`  
		Last Modified: Tue, 21 Apr 2026 23:19:17 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117903d566fb242d0e204c50e61a67e02a8c14a009223e8c11b267f626229584`  
		Last Modified: Tue, 21 Apr 2026 23:19:17 GMT  
		Size: 887.1 KB (887112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f135eb3614860c3231844c1c752f3927ddce77fb6fcf516c539fe6ac6fe9a2`  
		Last Modified: Tue, 21 Apr 2026 23:19:17 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67ae9ac7636228013de910de062582ed3035f80eb526b3c267885dd5d6aec37`  
		Last Modified: Tue, 21 Apr 2026 23:19:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6926a9ff8c416a22ff58bdaa895daa05c205cbd31e8af5b66801e30488736d2`  
		Last Modified: Tue, 21 Apr 2026 23:19:21 GMT  
		Size: 84.2 MB (84173496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550371b12ce469d6403e747825006909724ea9dfc1320594d7b40388766d7a28`  
		Last Modified: Tue, 21 Apr 2026 23:19:19 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0e489bb8910387ee3901da5d4e186836f883c0f7443bd78cb0df14657c6228`  
		Last Modified: Tue, 21 Apr 2026 23:19:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a7d92238717d9b8dfabbed460b4ea888e6f9ddd7d2edfa691dd354612753f6`  
		Last Modified: Tue, 21 Apr 2026 23:19:19 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728470acb967749cb3fa3f4b4bb175574ae748789586c054249aba191e5c5947`  
		Last Modified: Tue, 21 Apr 2026 23:19:20 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9812742c37bcdc2751c07713cd5dc35ff4086639a972ffb159fc1b0b7a86dc4`  
		Last Modified: Tue, 21 Apr 2026 23:19:20 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:608828f4ec028c853d14c9af56a282bce72a2745975182c3404787d95e72f639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 KB (44352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e9c85e4c1005eb03c72003a469dbc598e23236dbc05010895e7e1d78c29682`

```dockerfile
```

-	Layers:
	-	`sha256:5b4dbaa426be3a35261ebac408ef8b4b6b764127d8862995ded050ad9f5c3299`  
		Last Modified: Tue, 21 Apr 2026 23:19:17 GMT  
		Size: 44.4 KB (44352 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:12567c67815158dd2a115cc87e65e8a250e8f372f90111ef0f836d2f88665f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83895903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b9167773bad4c3bf1b904734a7e7d7957a5a434a82ffb4509cdaab7485b792`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:36:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:36:18 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:36:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:36:18 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 21 Apr 2026 23:36:18 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:36:18 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:36:18 GMT
ENV PG_MAJOR=15
# Tue, 21 Apr 2026 23:36:18 GMT
ENV PG_VERSION=15.17
# Tue, 21 Apr 2026 23:36:18 GMT
ENV PG_SHA256=ae14f24c14727e0b2ded1c5553031666099bd1054db3ef44bfa6e2bd6d554a56
# Tue, 21 Apr 2026 23:36:18 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:39:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:39:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:39:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:39:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Apr 2026 23:39:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 21 Apr 2026 23:39:01 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:39:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:39:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:39:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:39:01 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:39:01 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:39:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856f214be977f8b813c31348e4a3c1b73eddb595b6aa632b428650f020ad0964`  
		Last Modified: Tue, 21 Apr 2026 23:39:13 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9be6c27fcd6ad5c9a9dd4ad4b9955009b2e44e003936a2a42cefbf24ed8bba4`  
		Last Modified: Tue, 21 Apr 2026 23:39:13 GMT  
		Size: 887.1 KB (887123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0317de0846692d8fa8a9b5de95643ddbcfc365e10002f741a757c99456401c`  
		Last Modified: Tue, 21 Apr 2026 23:39:13 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa642d7b40b4257f14a4c05d61f008b0545c3ca2977ab91965cd3d31f8dd5af`  
		Last Modified: Tue, 21 Apr 2026 23:39:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8a8bae736393d4d2d8484df5437816aa2c669657d2eb5613408e0d0d5286cc`  
		Last Modified: Tue, 21 Apr 2026 23:39:16 GMT  
		Size: 79.7 MB (79708372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd34a302b4d4d7547fbe352d017e310ce98bd62cce3e358f36d759e96de2325b`  
		Last Modified: Tue, 21 Apr 2026 23:39:14 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591258256db35c575b6ea26e4e8374f4bdecd14214ee7544fcb9ba243b1021f4`  
		Last Modified: Tue, 21 Apr 2026 23:39:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70a894cfd7ad91b7e6275fab796b54e500ae53dd916184bc99718c7501c021c`  
		Last Modified: Tue, 21 Apr 2026 23:39:15 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e5dce11f25f2f390ddc8d42fdef1e506a450b66bec94ec47ebc542d551c4bc`  
		Last Modified: Tue, 21 Apr 2026 23:39:15 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4c333ddce23a3dc0d6d3278cb23e2bb469b89adf15384329823d5d57c69e4`  
		Last Modified: Tue, 21 Apr 2026 23:39:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:957fbff8d1b2cb901572ce54059f3c08d5745ca18238142990866a11197f270f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.1 KB (642062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694b8a655b841eff52ac90b9b61eb3522e706e8d7b64a3a1d942b520a5aee330`

```dockerfile
```

-	Layers:
	-	`sha256:0059011a28a7af547b77c23b9b7fbb9a22712c550a8076ad6077daf10cd7360a`  
		Last Modified: Tue, 21 Apr 2026 23:39:13 GMT  
		Size: 597.5 KB (597494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b3b4301ce968c517e17549bcf753ad6dbf3761021a71a6a8508547151d01e16`  
		Last Modified: Tue, 21 Apr 2026 23:39:13 GMT  
		Size: 44.6 KB (44568 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:c4b7ba83911c18ae85eeb1e45af0055e00c83e1eea43935711b872a7f8e6c194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107348164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1032c552baa1b9936393b7f6e5e7db3bcbf5705a62a28bd81caa22309588ac63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:09:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:09:26 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:09:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:09:26 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 21 Apr 2026 23:09:26 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:09:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:09:26 GMT
ENV PG_MAJOR=15
# Tue, 21 Apr 2026 23:09:26 GMT
ENV PG_VERSION=15.17
# Tue, 21 Apr 2026 23:09:26 GMT
ENV PG_SHA256=ae14f24c14727e0b2ded1c5553031666099bd1054db3ef44bfa6e2bd6d554a56
# Tue, 21 Apr 2026 23:09:26 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:11:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:11:38 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:11:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:11:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Apr 2026 23:11:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 21 Apr 2026 23:11:38 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:11:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:11:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:11:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:11:38 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:11:38 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:11:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4377d5b6adc110d16bfa0259707957e0ce7013640a86704dd74185484066cb68`  
		Last Modified: Tue, 21 Apr 2026 23:11:53 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d9e63c5c247d18e6ee2dcb5f3e9649ca6966786bb7fd19e1f6737be43a43b4`  
		Last Modified: Tue, 21 Apr 2026 23:11:53 GMT  
		Size: 874.7 KB (874714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fffb0cb0e4c59c31b9cbf2bb6815e41bbfe91d590cf6bdfd1f14c3c23ee24d`  
		Last Modified: Tue, 21 Apr 2026 23:11:53 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad8df76fc80a53a62a497a8ce0fb8706c326727a6f5c7c932593f53edfe0a5f`  
		Last Modified: Tue, 21 Apr 2026 23:11:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7160521737dd81d732ac1d1e3e46bbb78416c34e9316c86ac37cb94c55f964`  
		Last Modified: Tue, 21 Apr 2026 23:11:57 GMT  
		Size: 102.3 MB (102256293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d55f1d2e58403955aaf6d57dd4445fa4f514c38917d0ed8ad79131bf6ce61ec`  
		Last Modified: Tue, 21 Apr 2026 23:11:54 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c584142954e25e7a2ba327b244f51f8d0bda68560cac9cbe09a6203b0148187`  
		Last Modified: Tue, 21 Apr 2026 23:11:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a85e446412579c9c9e4f25fb290410df25673df8640b8522d961a314c24ce2`  
		Last Modified: Tue, 21 Apr 2026 23:11:54 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97afa9fbda77ecf55b6e6a5b93054b17ac8eecc5976b09cc011bfac7f402a7be`  
		Last Modified: Tue, 21 Apr 2026 23:11:56 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389a7cfae7deb67f4c9e01bcda62ed69a142bb105d27a51b3475689c8d0ee81c`  
		Last Modified: Tue, 21 Apr 2026 23:11:56 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:106b7318758f098608396476b8314f9fdae1d6c3c3286ead78b47a68cbf42803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.1 KB (642128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db45bae9edce8f591fe938e7f792c35bd6d4b632b325809a175ce983cf10e7a`

```dockerfile
```

-	Layers:
	-	`sha256:ebff895b6141fdba77381abf6ce27e15111c557b6953590757f9ee7c9ba94d89`  
		Last Modified: Tue, 21 Apr 2026 23:11:53 GMT  
		Size: 597.5 KB (597514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aad365d32b737abe9d8233b561818941e397430c4275dba826afe7c674fb75d0`  
		Last Modified: Tue, 21 Apr 2026 23:11:53 GMT  
		Size: 44.6 KB (44614 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; 386

```console
$ docker pull postgres@sha256:882576d440a9d1b3cda245ac8ee16a6b1c0b677a68138453cabd3e20cd06ec5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.2 MB (115210107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ebab726ce4bf605a8e288cb02f55595349816f099e708923173a941dcecd87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:15:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 21 Apr 2026 23:15:18 GMT
ENV GOSU_VERSION=1.19
# Tue, 21 Apr 2026 23:15:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Apr 2026 23:15:18 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Tue, 21 Apr 2026 23:15:18 GMT
ENV LANG=en_US.utf8
# Tue, 21 Apr 2026 23:15:18 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Apr 2026 23:15:18 GMT
ENV PG_MAJOR=15
# Tue, 21 Apr 2026 23:15:18 GMT
ENV PG_VERSION=15.17
# Tue, 21 Apr 2026 23:15:18 GMT
ENV PG_SHA256=ae14f24c14727e0b2ded1c5553031666099bd1054db3ef44bfa6e2bd6d554a56
# Tue, 21 Apr 2026 23:15:18 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:17:42 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:17:42 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:17:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:17:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Apr 2026 23:17:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 21 Apr 2026 23:17:42 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:17:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:17:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:17:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:17:42 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:17:42 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:17:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9725ff196d61a24c41d17f58262fb93e9f991fb0f743a7e0691f14c044a56e6`  
		Last Modified: Tue, 21 Apr 2026 23:17:58 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed279c6555471a55a488619b4be60bf8d6b8d5ff752488f624aed3d495256806`  
		Last Modified: Tue, 21 Apr 2026 23:17:58 GMT  
		Size: 891.6 KB (891645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f0a98a2482673f22caafd03247c2ddbe99885d0b0473de9fcb30797a2fd1c9`  
		Last Modified: Tue, 21 Apr 2026 23:17:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59052b9efe2504b4dfa38b7a47d64fafac779ca15c83faf29b6dcbb87c4f183`  
		Last Modified: Tue, 21 Apr 2026 23:17:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019549fa91667eddea7af4e41423a0a729bb4e73bfe77e719629d171fab8e396`  
		Last Modified: Tue, 21 Apr 2026 23:18:02 GMT  
		Size: 110.6 MB (110610740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ff682f579a79911e44a122bcdbc1ca8166037448263d71cf83e28bd04d801c`  
		Last Modified: Tue, 21 Apr 2026 23:17:59 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8f964811c65aa4f7271840a26d1d52ddec27f60fac19955ba3916e4f1c0242`  
		Last Modified: Tue, 21 Apr 2026 23:17:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583fe2abda655acf47df98f18cd712b70bf4c011aaa7b263c09ac9d4e96fa993`  
		Last Modified: Tue, 21 Apr 2026 23:17:59 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3a6f3a984ff7651fe865973f1792b1a1283fe283538312f090ea7f61c99e6b`  
		Last Modified: Tue, 21 Apr 2026 23:18:00 GMT  
		Size: 6.1 KB (6094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec73cfa928a0bc7a07d9d31a7cde008f07ba71e97fc2b4fcce100504519c158e`  
		Last Modified: Tue, 21 Apr 2026 23:18:00 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:a0ba1ed45261b2c9445a703d91815738fe61a6559b3d416d9248c00765f8bf84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.4 KB (642424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f79923021eb76672de0f41f98a4fa395de868c4a704719ddb9a98fe4ac8dc2e`

```dockerfile
```

-	Layers:
	-	`sha256:74de88da463afb3c89fe43e9a6fd37efd969cf783f5cc860c523e6d3adb24f03`  
		Last Modified: Tue, 21 Apr 2026 23:17:58 GMT  
		Size: 598.1 KB (598083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f7be7ac5bf5324441b10e27e27d7789ffbf8e091adaf5ce180b096066c03023`  
		Last Modified: Tue, 21 Apr 2026 23:17:58 GMT  
		Size: 44.3 KB (44341 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:5cf2b09153ddc1b1791ff577dc7dcc001a812bb1742b9a8bf699326623afdd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94062322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26cfb7af4af13e82d0a94541f34acc7385f281f9a9ec9da70efef7eb3710c3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:55:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Apr 2026 20:55:24 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:55:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 21:00:23 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 15 Apr 2026 21:00:23 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 21:00:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 21:00:23 GMT
ENV PG_MAJOR=15
# Wed, 15 Apr 2026 21:00:23 GMT
ENV PG_VERSION=15.17
# Wed, 15 Apr 2026 21:00:23 GMT
ENV PG_SHA256=ae14f24c14727e0b2ded1c5553031666099bd1054db3ef44bfa6e2bd6d554a56
# Wed, 15 Apr 2026 21:00:23 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Wed, 15 Apr 2026 21:04:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Wed, 15 Apr 2026 21:04:26 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Apr 2026 21:04:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Apr 2026 21:04:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 15 Apr 2026 21:04:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 15 Apr 2026 21:04:27 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:50:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:50:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:50:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:50:20 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:50:20 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:50:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9504179c89581170cbe497b214c2f97f01eae1cac5905e1d1fafdcf5bc01926d`  
		Last Modified: Wed, 15 Apr 2026 20:59:59 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a284924cfe2e8e2e82ff8309f349edbdfa04cfaa5de86e49b14e6cb75225a`  
		Last Modified: Wed, 15 Apr 2026 20:59:59 GMT  
		Size: 880.1 KB (880126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdbf69e74f8065c17f9aae6946c699680b19b0f5dac3b0eb9d86c6b4d150805`  
		Last Modified: Wed, 15 Apr 2026 21:04:25 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40505d0bc2ac480cc189bc63f3786b58510be6cd3ab7577555a65b6258920690`  
		Last Modified: Wed, 15 Apr 2026 21:04:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef229b7e6ca0317b897912c3c6fc5ba42f50de7cb5c14a9c77f324308639f504`  
		Last Modified: Wed, 15 Apr 2026 21:04:58 GMT  
		Size: 89.3 MB (89333955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc5c666242fd2ac877ff50f41f3c3c700c9cbe79669932c8d7aca6397a8de6a`  
		Last Modified: Wed, 15 Apr 2026 21:04:55 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185f9972084976d61abf2a3c22424cf1bdf7e21decaf915624b616e819978503`  
		Last Modified: Wed, 15 Apr 2026 21:04:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45067d6ce7a21b6c672b1133a3a2088259c93de306eac4dff4f3a958a3aa8488`  
		Last Modified: Wed, 15 Apr 2026 21:04:55 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328cbb651ded81c615ce46ff0743c2cc3f64717f4e1a13f07ae7416dc2005fa2`  
		Last Modified: Tue, 21 Apr 2026 23:50:42 GMT  
		Size: 6.1 KB (6104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f2a69729188bd43614e26b21e187525ba9d10102e5ff89fa9926e411f6768c`  
		Last Modified: Tue, 21 Apr 2026 23:50:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:33600f13bc26c535099beb70efba67e229a424983d577e6203af3a1d0c013f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.3 KB (640273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70dc7e40a2ad41c7ef9a56f51ec0000681afcb980c5fd860732d89061a63a88`

```dockerfile
```

-	Layers:
	-	`sha256:06e4e23c75b03f7b55974ca2f3b86b405ce2af64115dc41220fe9f829ce591ad`  
		Last Modified: Tue, 21 Apr 2026 23:50:42 GMT  
		Size: 595.8 KB (595829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a7fd22fd35314c4d4a8c0d9633b7ccc566736797ac1c990a3c5a69fd924d0b0`  
		Last Modified: Tue, 21 Apr 2026 23:50:42 GMT  
		Size: 44.4 KB (44444 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:d2da5579bfa593a143cfec9c3323f00afe7bb21bee8711b7fcb0aff577c63f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110149866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608769a73d8133f2df91a7cadb3aaabf3185bf50ca7546ed148274dc13f15f35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 11:29:33 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 16 Apr 2026 11:29:45 GMT
ENV GOSU_VERSION=1.19
# Thu, 16 Apr 2026 11:29:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 16 Apr 2026 13:20:58 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 16 Apr 2026 13:20:58 GMT
ENV LANG=en_US.utf8
# Thu, 16 Apr 2026 13:20:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Apr 2026 13:20:59 GMT
ENV PG_MAJOR=15
# Thu, 16 Apr 2026 13:20:59 GMT
ENV PG_VERSION=15.17
# Thu, 16 Apr 2026 13:20:59 GMT
ENV PG_SHA256=ae14f24c14727e0b2ded1c5553031666099bd1054db3ef44bfa6e2bd6d554a56
# Thu, 16 Apr 2026 13:20:59 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Thu, 16 Apr 2026 15:03:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 16 Apr 2026 15:03:49 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 16 Apr 2026 15:03:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 16 Apr 2026 15:03:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 16 Apr 2026 15:03:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 16 Apr 2026 15:03:49 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 16 Apr 2026 15:03:50 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 15:03:50 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 16 Apr 2026 15:03:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 15:03:50 GMT
STOPSIGNAL SIGINT
# Thu, 16 Apr 2026 15:03:50 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 16 Apr 2026 15:03:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c05352c3bc3bad2a071af544c560bfc66f25f632b9841754ed94c4abb19732`  
		Last Modified: Thu, 16 Apr 2026 12:22:58 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0841d6e8e03b3f5779ff0c2893e4e26e90895e6f4a7ec62726ad628be33e10e`  
		Last Modified: Thu, 16 Apr 2026 12:22:58 GMT  
		Size: 867.5 KB (867538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01640490039f18e0efc72dfc7e79e994ee5239169b238b30d21ba147a4d3d087`  
		Last Modified: Thu, 16 Apr 2026 14:14:12 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba82bcb214ae71de3d2b623be98402bc90b03aef6f555c7dd3f2d1a2a3676e2`  
		Last Modified: Thu, 16 Apr 2026 14:14:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be77d9005e33b8f3c5ea64fb271b287c255adc6232163e9fb6db86d552dd3a98`  
		Last Modified: Thu, 16 Apr 2026 15:06:49 GMT  
		Size: 105.7 MB (105677621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a953d9684a69a9292146d40197d4a61262ed078f4010121aa73f1d50c785cfb4`  
		Last Modified: Thu, 16 Apr 2026 15:06:34 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73842c27b3aa90b2e73bea5af116c108349ff0409229584b7cf2fd365d1e76bc`  
		Last Modified: Thu, 16 Apr 2026 15:06:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ee51387bc714cb84082a4a28fcd274f01fe7acacf6acedafafd0f8e4f1000e`  
		Last Modified: Thu, 16 Apr 2026 15:06:34 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78b945566dca3de35cfcd868b656535eed4e902dff431dcf87e394957026d75`  
		Last Modified: Thu, 16 Apr 2026 15:06:36 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51ab6940aea740fd1b1c992b13c17db6b9e626d9594913e85a4f14995adffcf`  
		Last Modified: Thu, 16 Apr 2026 15:06:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:28fc6e88fc0946b9cfe9b755b4f49ac2211d047f588699c6c78d70e4de8d71e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.9 KB (641937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab50e59bb745daf750df9f778b7e9b778bd64974f5983401d00d0ec880309c7`

```dockerfile
```

-	Layers:
	-	`sha256:ed84b060e2a9dd05da096184d7ed6aaf06079ebb3ec22c549efbaad9733437a9`  
		Last Modified: Thu, 16 Apr 2026 15:06:34 GMT  
		Size: 597.5 KB (597487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cef057aaedb4dbd723975930ada259571ea17a4aad37dcbff24a62758868cca1`  
		Last Modified: Thu, 16 Apr 2026 15:06:34 GMT  
		Size: 44.5 KB (44450 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:bd346c12c8f8c2feda454b2ab4869fe339b246131ffdb81c7bbec323c7ba6c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117301011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c0b5b8c0a420d2bb1d7bdbbc0a77cb8aba691d8484f742932932eec156be6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:32:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Apr 2026 20:32:28 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Apr 2026 20:32:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Apr 2026 20:37:51 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Wed, 15 Apr 2026 20:37:51 GMT
ENV LANG=en_US.utf8
# Wed, 15 Apr 2026 20:37:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:37:51 GMT
ENV PG_MAJOR=15
# Wed, 15 Apr 2026 20:37:51 GMT
ENV PG_VERSION=15.17
# Wed, 15 Apr 2026 20:37:51 GMT
ENV PG_SHA256=ae14f24c14727e0b2ded1c5553031666099bd1054db3ef44bfa6e2bd6d554a56
# Wed, 15 Apr 2026 20:37:51 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Tue, 21 Apr 2026 23:41:54 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-icu 		--with-ldap 		--with-libxml 		--with-libxslt 		--with-llvm 		--with-lz4 		--with-openssl 		--with-perl 		--with-python 		--with-tcl 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Tue, 21 Apr 2026 23:41:54 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 21 Apr 2026 23:41:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 21 Apr 2026 23:41:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 21 Apr 2026 23:41:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 21 Apr 2026 23:41:54 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 21 Apr 2026 23:41:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 21 Apr 2026 23:41:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 21 Apr 2026 23:41:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Apr 2026 23:41:54 GMT
STOPSIGNAL SIGINT
# Tue, 21 Apr 2026 23:41:54 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 21 Apr 2026 23:41:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c5ed854292088ad91fb5a623e51a3682312408cead42a22166de3fd8d1dc8a`  
		Last Modified: Wed, 15 Apr 2026 20:37:29 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ce62b957b857c08f679922ba4b91dc49057c951937637dd94b40a7fe8c5b81`  
		Last Modified: Wed, 15 Apr 2026 20:37:29 GMT  
		Size: 895.8 KB (895798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae20370d30162e578ddc4261332750d5420660a4b540ba6effcd03e08803223b`  
		Last Modified: Wed, 15 Apr 2026 20:42:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2957e716cf88c06abe669da7b50ef11d5b4dd8a2518ba299f5cc206a57082586`  
		Last Modified: Wed, 15 Apr 2026 20:42:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e52ced43a4a1447ddf3456e7d14fe321e6fc41d9bd8fd81930278bf574e9e02`  
		Last Modified: Tue, 21 Apr 2026 23:42:26 GMT  
		Size: 112.7 MB (112661386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfad5fe5621c5af70f0674f8ecc599f640d031d4584a5d1ccc973f902386291`  
		Last Modified: Tue, 21 Apr 2026 23:42:23 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c126b5fe5ada95fd94d41174d78e6ea68791c4e3bd57fe3bb3f1982382456f`  
		Last Modified: Tue, 21 Apr 2026 23:42:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774373195918e8414f458ffe7245368c44f84174f601c6e5243b52028d837947`  
		Last Modified: Tue, 21 Apr 2026 23:42:23 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373ac9aa35d42a70c573921aae4f424ed6b49ec5aee8d250a0ac7e4317c2339a`  
		Last Modified: Tue, 21 Apr 2026 23:42:24 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60e68deebac758c3bd80fef7692030770eb344e17593ca963c27990a9318794`  
		Last Modified: Tue, 21 Apr 2026 23:42:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:3ab79022bba35873c420ac0baef6c0afd2d63a8d1f9040dc83b81da6731bcde9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.8 KB (641846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504fac412b4defce68f37fb44836bda90852ab01f124d5f536d0946ae2bb87e8`

```dockerfile
```

-	Layers:
	-	`sha256:7d2227585e69a29f722693ef531bb731f2c837457ba3d55e7da6de97aac1f542`  
		Last Modified: Tue, 21 Apr 2026 23:42:24 GMT  
		Size: 597.5 KB (597457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d641dca2aaf1326771a8baa0340e214c553faeb8ef8ea699229986d55611b0`  
		Last Modified: Tue, 21 Apr 2026 23:42:23 GMT  
		Size: 44.4 KB (44389 bytes)  
		MIME: application/vnd.in-toto+json
