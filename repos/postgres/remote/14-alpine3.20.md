## `postgres:14-alpine3.20`

```console
$ docker pull postgres@sha256:55a42b2d0288ab6734f65d4aa262f85a92f80af14c357f1a2880ec439783fb01
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

### `postgres:14-alpine3.20` - linux; amd64

```console
$ docker pull postgres@sha256:ed1c9c420ec7b95257b057326a53defd0919009fb102baccaa5cb45ad335f7b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97637473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638c4cf7d9b9872b57043b0fc1eccf40852e99b192876e009536c13243900fd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_SHA256=59aa3c4b495ab26a9ec69f3ad0a0228c51f0fe6facf3634dfad4d1197d613a56
# Thu, 08 Aug 2024 16:52:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8494eb6e60d49ea8614ea6e1dc5b9b0d5b544c0b9b6daa20489b1574deb076e0`  
		Last Modified: Tue, 12 Nov 2024 02:37:58 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7820f88ab0e50a90116b4a4e89ed25f1d27325f55354860d969866b183c23e`  
		Last Modified: Tue, 12 Nov 2024 02:37:58 GMT  
		Size: 1.1 MB (1119766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1229951d7bca5fcbd2938a18144382426be93b804ea48e19bfc5f7bab2d1494a`  
		Last Modified: Tue, 12 Nov 2024 02:37:58 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20aab744d539d5ccdc1d3e6914a244fb060f804ff79174114642e607a0a74807`  
		Last Modified: Tue, 12 Nov 2024 02:37:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37266450a5f9f5ae8c117dabe872b459dd07bc59dc0ee932a4fd47e2ba389b4b`  
		Last Modified: Tue, 12 Nov 2024 02:38:00 GMT  
		Size: 92.9 MB (92877424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0723ef03a97f2ec325a7cbbd8ddb092c7d1c46884c711939d3a02600c6b947`  
		Last Modified: Tue, 12 Nov 2024 02:37:59 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15e71dfbb2248d46ed7c6611c0fa7179841cee782bdc0643c0433b9bfee8d33`  
		Last Modified: Tue, 12 Nov 2024 02:37:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3e8948348d12241a4259a47bba4cfd746a891bc6671a78f5ca7db2c5388f32`  
		Last Modified: Tue, 12 Nov 2024 02:37:59 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7cdab9cfb5ef5a3067b6da17244627fa391192e6eb881af493161dd3d3ae4c`  
		Last Modified: Tue, 12 Nov 2024 02:38:00 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41b68640e188f9f646635988d4dd32f82a45ecb3e424615faf51d66a038c78d`  
		Last Modified: Tue, 12 Nov 2024 02:38:00 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:3be16d7ab32803294d63f1b91b082e54cee829e1103d28f74bb70f90df5cf284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.6 KB (636612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871128b31916bdd33439ace1aa06ab866e98e4e9e2f6dd9801231f9d88d01ad6`

```dockerfile
```

-	Layers:
	-	`sha256:2f380da7a42a5f4575223b8f0e0b1c9d223023f6ea3f2e6f2a483ab188e59991`  
		Last Modified: Tue, 12 Nov 2024 02:37:58 GMT  
		Size: 591.0 KB (591021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfeffe297dd0656a657634ee51432cf2f9c6df034a87d24b214c1633d8a36f0b`  
		Last Modified: Tue, 12 Nov 2024 02:37:58 GMT  
		Size: 45.6 KB (45591 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:a685a2d0eaaeb801f17e54d8731661113d0f705c1b9121e0dcbea925c8c3f679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96072449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36dae19410ed5ba6262c3997ba300bd1a3fbf71a786e9d527802731491190be9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_SHA256=59aa3c4b495ab26a9ec69f3ad0a0228c51f0fe6facf3634dfad4d1197d613a56
# Thu, 08 Aug 2024 16:52:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c571936168ff49222fc45202f5453daceaaad85841344e7a56766ac0c06bcc0b`  
		Last Modified: Tue, 12 Nov 2024 05:37:05 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd27d05dad1bb8227f4e72ddcbdcd2601f74b55f8b2929cff613d173bc82672`  
		Last Modified: Tue, 12 Nov 2024 05:37:05 GMT  
		Size: 1.1 MB (1086464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68300102007bc93827d658bcc2e3930a994d78385553143780dadcc3f284915a`  
		Last Modified: Tue, 12 Nov 2024 05:45:35 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef5933ae7af9d77048b5e8ce8dc6807af55c837feaeaecb0fac68b44b61199d`  
		Last Modified: Tue, 12 Nov 2024 05:45:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5df5222d0822c985d72e6ac3bf8fdc55bf02aec9b06b89bb62270391b3fa8d8`  
		Last Modified: Tue, 12 Nov 2024 06:01:29 GMT  
		Size: 91.6 MB (91603008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cf30ccaa24eed05d75b2e231c85ae0d9004049b0794a1c10dacfabb8c36993`  
		Last Modified: Tue, 12 Nov 2024 06:01:26 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cb3a6577cd21294f9fc3b36061109bf8af8c717320d56851ae2b50e9d1e1ca`  
		Last Modified: Tue, 12 Nov 2024 06:01:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f25cb448eaeed8356ecd1445ce73d6ede329c505ff8e5002d3dc04544711ca`  
		Last Modified: Tue, 12 Nov 2024 06:01:26 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3a7465706e3e8eed111f2cdcfaee5da22a7e643a6217ac13e07b97a45bf0f8`  
		Last Modified: Tue, 12 Nov 2024 06:01:27 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d685b0cde4ed1a13b85cb6685605731889be79374fdffc4e5c98ac990647967`  
		Last Modified: Tue, 12 Nov 2024 06:01:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:c90870179aa5bc3cc0b75f3eec431a985915bf7f01c335fcbff56b14a7b19215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 KB (45556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f052a8aaebc0eafa95dab71903200e14bcf84b685bc3b7351ed4f5b0b4a224b`

```dockerfile
```

-	Layers:
	-	`sha256:d49ba149ec7508b46dde311b23ebb6fefb9d194c82b92d1d6024ae9ec4784670`  
		Last Modified: Tue, 12 Nov 2024 06:01:26 GMT  
		Size: 45.6 KB (45556 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:aa0476b13f6badb89877c769ba95e1a985074ed4aa4adbe6d1d202d46301d7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88560467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:970892a6aab96ceb9225c8c6a2092b2fdfe99dff90814fae9bc02ccbdecf6126`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_SHA256=59aa3c4b495ab26a9ec69f3ad0a0228c51f0fe6facf3634dfad4d1197d613a56
# Thu, 08 Aug 2024 16:52:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ac8e9d0c68b096b09818bfb20f42e953c3d9cd9df375198a3b549dd5ce5f63`  
		Last Modified: Sat, 07 Sep 2024 09:07:01 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea95758d71d5413b7fd57d98797bffda5c623934cbefc0067a635c1ff9f62e9`  
		Last Modified: Sat, 07 Sep 2024 09:07:02 GMT  
		Size: 1.1 MB (1086468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f93540d99e99914202c8ed07dbb4762ba225d2c6061670c2fafc29c7af5b206`  
		Last Modified: Sat, 07 Sep 2024 09:15:08 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8913630691ba9994e15bc5ad692e83b0d35705f5db68d326926e420ae066c0e7`  
		Last Modified: Sat, 07 Sep 2024 09:15:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b064750e513ac4928c5582235a2305ee32ac78d07daf06ef8012195e357ee9`  
		Last Modified: Sat, 07 Sep 2024 09:30:16 GMT  
		Size: 84.4 MB (84362115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb4b6acce5e8d23b2564ec0cb83653ae7e257cc59718f6dce89e5a9dac53ba3`  
		Last Modified: Sat, 07 Sep 2024 09:30:13 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdae7b4a47ed46e9bf5c1e5ca49bf478e04765b489659e00d725fc7b34949fd8`  
		Last Modified: Sat, 07 Sep 2024 09:30:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821463e1aa9678c35a36010b3c3de9565186569fe710abb9436110e9dd768ab8`  
		Last Modified: Sat, 07 Sep 2024 09:30:14 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b955af1b35c9bc48592849c5fae7cef87705c4f55c6f30080efb9265ac944082`  
		Last Modified: Sat, 07 Sep 2024 09:30:14 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cee6757edaf75845d7b0baa5c1dd5b369c92d5b0bb14088d356f66db7b92b9`  
		Last Modified: Sat, 07 Sep 2024 09:30:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:ceeafd3552215bc7069ad7af6a6003e48f0b24b9968e608021120bb1ce61c5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.3 KB (636313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8822f3e03e9f443d434e7564347486b42820cb891bddc6fd5fa96af82c82b93`

```dockerfile
```

-	Layers:
	-	`sha256:48e1aa7cb914d737067db4beade1b90883543e005cc445678f817f51c8ae9aad`  
		Last Modified: Sat, 07 Sep 2024 09:30:14 GMT  
		Size: 590.7 KB (590739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51f181ecf18d2e567134b79ac8cb57638495b3a6d6dd9dca33b3a9e036b94080`  
		Last Modified: Sat, 07 Sep 2024 09:30:13 GMT  
		Size: 45.6 KB (45574 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:5a0b05626cef4677cc43404bf0c571f801365fb618cbea38e635bd2cf02284b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94578688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfe1346c4470cae525ffa4d268868afae1df3157b38be3b3cea692349bbb169`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_SHA256=59aa3c4b495ab26a9ec69f3ad0a0228c51f0fe6facf3634dfad4d1197d613a56
# Thu, 08 Aug 2024 16:52:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce02d10b61bf34aa182aa7cd3783def4d5bbd8176c97011032c1508b214ff88`  
		Last Modified: Sat, 07 Sep 2024 08:43:43 GMT  
		Size: 987.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc2a136d16381dd1cb44173056502b63f1221519780ccd6a68b144efc25d984`  
		Last Modified: Sat, 07 Sep 2024 08:43:43 GMT  
		Size: 1.0 MB (1047249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ca8946873e79c55e98d72c8e8199b4e5fa08d6d8c68ef8a6901d7c0300fd2`  
		Last Modified: Sat, 07 Sep 2024 08:49:49 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e732be064c163369f8060a02cdb4896b04c1cdb30b10c1a5bb161a03df18d9`  
		Last Modified: Sat, 07 Sep 2024 08:49:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4867a0418fc0d9e5c89fe50d6688ec067aca5ed0b87afb12cd0d0480cb2cefa`  
		Last Modified: Sat, 07 Sep 2024 09:01:14 GMT  
		Size: 89.4 MB (89427412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61f80c00259767aeb38825f230eeb3929ef9ce4e490e317d686b4cfc474c16b`  
		Last Modified: Sat, 07 Sep 2024 09:01:12 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ea4790cd188ce01260b0e3222afb3c5df74575e02608e3556b1815a2abf229`  
		Last Modified: Sat, 07 Sep 2024 09:01:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb352d4e8faeab50860954da45b0ea70292f24629a231db7422433bd0f83cb18`  
		Last Modified: Sat, 07 Sep 2024 09:01:12 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f11a9a130ae71ce981ea19a992ba1f964224664bd8f351929a0781d27b5687`  
		Last Modified: Sat, 07 Sep 2024 09:01:12 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0308927099c5c7abdd3f1ddadee937b2a8ba2f07974999b283359c017bcd7a7f`  
		Last Modified: Sat, 07 Sep 2024 09:01:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:6df783410027fe825ea96a68156e1f2538788ce65e061e759bdefc5f6b80ad05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.5 KB (636458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d7e7b59152fffbafd138bfa1a2a8ee63a5e49ce5819f66511392513abece1d`

```dockerfile
```

-	Layers:
	-	`sha256:6497970813ef8e17a48597b03963aeec8ea8d9a1c54f0d09220865f43e9d7fd3`  
		Last Modified: Sat, 07 Sep 2024 09:01:12 GMT  
		Size: 590.8 KB (590759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c15460cde1afc9737c33c5dc5c0433662a9ec62b2cf85f1a3c27bf00bd14339`  
		Last Modified: Sat, 07 Sep 2024 09:01:12 GMT  
		Size: 45.7 KB (45699 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:719216aff08a0e26f2bded3bc4ee141950fd13a170ecc827d9c8fa0e049142d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102781112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b942f3f02ce51e06313ccee0283a46f1adac5fa6d3af9388b8dda36644e1722`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_SHA256=59aa3c4b495ab26a9ec69f3ad0a0228c51f0fe6facf3634dfad4d1197d613a56
# Thu, 08 Aug 2024 16:52:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f876a3ed3fe4b0dd53795c022a4b718dbecee7bc6877fbf9ffdcd8959e73dce`  
		Last Modified: Tue, 12 Nov 2024 02:38:24 GMT  
		Size: 982.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594ff84381b006b29aeeab5a3944d74008899f0541840de0db5f15486bf434b4`  
		Last Modified: Tue, 12 Nov 2024 02:38:25 GMT  
		Size: 1.1 MB (1094860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf025f95994d0019d48aee086f9c6695f68abf0b1387c3b916525a7886cf6f3`  
		Last Modified: Tue, 12 Nov 2024 02:38:24 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6bf0b74a292a06d34d4bcdc3e848c9d2247334d2dc07e1940b2a7953c94d8a`  
		Last Modified: Tue, 12 Nov 2024 02:38:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d400a250377e22efcc78b394bc384db71a6409834359c07f274103893a2a034d`  
		Last Modified: Tue, 12 Nov 2024 02:38:28 GMT  
		Size: 98.2 MB (98200662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fdbcc266814333c9a7e762567c93fc105d2913f94904b6dc8ebd7848c336de`  
		Last Modified: Tue, 12 Nov 2024 02:38:25 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6551fd7a695a38f8e59323e029d5b59e8324c02d84f7fb0ee17b0fc53c6d2a`  
		Last Modified: Tue, 12 Nov 2024 02:38:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e0084c4d4987af7434d4ccc738d3c104327c1269797a6b398e6a8ba50af0dd`  
		Last Modified: Tue, 12 Nov 2024 02:38:25 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5227fc9a23f3c41169bf14114c8ba498f351bd4d4a20773a403b067fba46b2`  
		Last Modified: Tue, 12 Nov 2024 02:38:26 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f26173bf2f057e0671c2c4e59fd56efa9b5ac15d1374da095a6f3875ee659c`  
		Last Modified: Tue, 12 Nov 2024 02:38:26 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:2d86292e607542fcc05dd07105ce015a52dbb44700d08b870985b1dcf25f56ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.5 KB (636539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590057c3d17760875b9593b26d326a27fe7def07049fcec164978cdd69cefe85`

```dockerfile
```

-	Layers:
	-	`sha256:68f6bd6a89c5999cede75fa4c71b7434f33cedbe5352ecdf11601b16a3c1e2d5`  
		Last Modified: Tue, 12 Nov 2024 02:38:25 GMT  
		Size: 591.0 KB (590996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ded90c996c8ea7346a3ebc4b582a3ef111052a8e87b9af72be064584b03d1e1`  
		Last Modified: Tue, 12 Nov 2024 02:38:25 GMT  
		Size: 45.5 KB (45543 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:483d8939e644cb3ad6ed897a4d6deea6938f5bcb271805ba7f06b890066a6282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102008238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71057c12e251de28182b06e8d10145562b9326a8ad387fd6b1b628b81d568eba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_SHA256=59aa3c4b495ab26a9ec69f3ad0a0228c51f0fe6facf3634dfad4d1197d613a56
# Thu, 08 Aug 2024 16:52:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19a7a1f04747157cc38c8ea66a5ff6b25a502c971bf6b56995e5fefa252c706`  
		Last Modified: Tue, 12 Nov 2024 07:00:20 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1f73e281b372894f9fde9cf8b361dac11c7e4a99a9be8741f261633ef51c5c`  
		Last Modified: Tue, 12 Nov 2024 07:00:20 GMT  
		Size: 1.0 MB (1037936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eacc863115d916c7f14fdb7956d45a06cd56072bfcb39abee699970ca8aff`  
		Last Modified: Tue, 12 Nov 2024 07:09:39 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f4827aec3ef0953d51b1267885e898aa3f3f28676e7230bb67120dd71f28c2`  
		Last Modified: Tue, 12 Nov 2024 07:09:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d70fc9055f41a4f96ac54b6cdb1696c61bdd8eaeb78840bb8d7147a48b4e67`  
		Last Modified: Tue, 12 Nov 2024 07:26:56 GMT  
		Size: 97.4 MB (97381458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab92ea6f474afd53efba18ebfb14aa009b01d4bd925d8753ab04d6257dfb4e4`  
		Last Modified: Tue, 12 Nov 2024 07:26:53 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336800fb09e2746c43495b50fe985eabe3d1cc693dd397bc4653bcf9b45d6e4f`  
		Last Modified: Tue, 12 Nov 2024 07:26:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb89f6ee9c7d9483279cbfa315c70f62288a7854b714e8719758090b5e1c0997`  
		Last Modified: Tue, 12 Nov 2024 07:26:53 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b06cc73f5c6ad9758c4a55411a7fbd4868c00a67338da1f928cbf9d038e08a6`  
		Last Modified: Tue, 12 Nov 2024 07:26:54 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7223b093e7c162f238187c3735244317d411a6254202f63042e5efb9d6439a0`  
		Last Modified: Tue, 12 Nov 2024 07:26:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:75156790f9850cb3c5a133f6dc0860a627b823d9df5b5e5e605356b99034303f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.1 KB (633088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d44eda20a73f938365fea1ca9f71487835b3905427200069bb0d4d740299d7`

```dockerfile
```

-	Layers:
	-	`sha256:736c2509c24339fe75221c9f21e8c553aef8041af94a0af3cb53c9ecaa946b07`  
		Last Modified: Tue, 12 Nov 2024 07:26:53 GMT  
		Size: 587.4 KB (587437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeb724378aa093b80bd540f64de0800cbaea8c0c29cefa8dc7772850b3a5072c`  
		Last Modified: Tue, 12 Nov 2024 07:26:53 GMT  
		Size: 45.7 KB (45651 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.20` - linux; riscv64

```console
$ docker pull postgres@sha256:8717228aaa5c94ceb3718adfc9706680eae0f079f8f3c5e0a12a82f80fff44d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95480266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ba2f3688a9b08d507467faf5ed1ff5287de4f54daa760e9c79fac46ad441d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_SHA256=59aa3c4b495ab26a9ec69f3ad0a0228c51f0fe6facf3634dfad4d1197d613a56
# Thu, 08 Aug 2024 16:52:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c0a33ca1e0010b2933d844f58d1adbfedd0d5f9ed593d28f743f587da5c4f0`  
		Last Modified: Sat, 07 Sep 2024 21:37:02 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc8cc678fef78489c3aaa8bdfb1dcc8f823e88452890bd484cba0b49520c887`  
		Last Modified: Sat, 07 Sep 2024 21:37:02 GMT  
		Size: 1.1 MB (1087946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56080afd24856e1cc3534a3aa835dd8e919182dcbb4d29dec312b4b72463b1`  
		Last Modified: Sat, 07 Sep 2024 22:25:51 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6835e21d92909284f4c71469ba5da9d23258e4089d86e92014b58bd67c10397b`  
		Last Modified: Sat, 07 Sep 2024 22:25:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e40a80c3486fb7e1322467c280300120048e539a8375491cea358b81f538720`  
		Last Modified: Sun, 08 Sep 2024 00:25:58 GMT  
		Size: 91.0 MB (91004473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233139c674955fd1cb6df6fa8a01c2b2fdbedfadc3304f0d4a882a10302c1656`  
		Last Modified: Sun, 08 Sep 2024 00:25:45 GMT  
		Size: 9.2 KB (9210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed929ee28d879a4c6a661a39b155c5effcb80643e38196bd1157d2140ce6294`  
		Last Modified: Sun, 08 Sep 2024 00:25:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb892d0e6ec978d0969ef4a0f7c1f19bf48e6d356fd1e97afbd1ae402eca66c7`  
		Last Modified: Sun, 08 Sep 2024 00:25:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abd29b6753074e407733d00657157ecc9227307d9b48b89ba29d26341a53da1`  
		Last Modified: Sun, 08 Sep 2024 00:25:46 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58340d3f7e97b6c02a78ee48c3490686ffa80614101b33ce70a6516f8c3531ce`  
		Last Modified: Sun, 08 Sep 2024 00:25:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:2c3ad5b8fd9db72c4026da5532f7280d72d35658d94397c68879d30a7d7130b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.2 KB (634233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa985076d8813e859e774406ace97aead8df23795297bfd54a7cb8315ff5b94`

```dockerfile
```

-	Layers:
	-	`sha256:ef081ac9def370687d408bd71cc472b6d549e363a10928287c8af524f4f3562b`  
		Last Modified: Sun, 08 Sep 2024 00:25:45 GMT  
		Size: 588.8 KB (588779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:864fbb4331337b0a2785f247dfb7583a42d68eba9e1d3be26047909e82bee99a`  
		Last Modified: Sun, 08 Sep 2024 00:25:45 GMT  
		Size: 45.5 KB (45454 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.20` - linux; s390x

```console
$ docker pull postgres@sha256:d4051d8af1e9c34afbbc16dbbdc0a298c2e913972f2cc8a75af949f0d93016af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106275128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e17015c35f17cd38bff60ae1ee8e6065ac167953c2e34d44d853ab5e9d63a40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_SHA256=59aa3c4b495ab26a9ec69f3ad0a0228c51f0fe6facf3634dfad4d1197d613a56
# Thu, 08 Aug 2024 16:52:20 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cfe172c7a286e8204df6e52175624b09a8eac0323a0ca93d64bb47b1e1d2ea`  
		Last Modified: Tue, 12 Nov 2024 07:35:14 GMT  
		Size: 989.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd3aae594b33f2c3d620dfd8f818b5fa3f522b0ebd8fa55dc50df0de8cb9062`  
		Last Modified: Tue, 12 Nov 2024 07:35:14 GMT  
		Size: 1.1 MB (1083302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fe6b14f6ff1c0c299e08d8735b27df365d66f54f2df01a42eebe9fdd7d36e8`  
		Last Modified: Tue, 12 Nov 2024 07:45:10 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475d6ddd0abdc1a91a6d685920d91fb766349ac3cc95c6ec4c29882d02db1665`  
		Last Modified: Tue, 12 Nov 2024 07:45:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0633d6e2c02060769b02fe2c6a1ca52af63a8f422984f4f2198a891fc89fcf`  
		Last Modified: Tue, 12 Nov 2024 08:03:15 GMT  
		Size: 101.7 MB (101713827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96032f95e3316bc2826a3114f23a941def52f2b79463a8ebf1965d0c4dc427ca`  
		Last Modified: Tue, 12 Nov 2024 08:03:12 GMT  
		Size: 9.2 KB (9208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e842c7a605f37ea4e985a5b29050e782995415cc46422298f9a2026b2ff5a7`  
		Last Modified: Tue, 12 Nov 2024 08:03:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af818d2d028e6a1a59238f74764a7182990bf8b50cd7f7804558c42f5c703296`  
		Last Modified: Tue, 12 Nov 2024 08:03:12 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7837fe5692826c59d0ca8156e68f488a426329a1b873ee6266b67e1e928d667`  
		Last Modified: Tue, 12 Nov 2024 08:03:13 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0392a2e72135b34812d91e0398eeb938d6050059ff14e07fb1a5faf6c3022fac`  
		Last Modified: Tue, 12 Nov 2024 08:03:13 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:19561d40aeecb131d02e4bb2faacb069168f3cacf4787bba29a8a1f6432b5fb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.7 KB (634664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71aaa714579028ce2bf22bf1565f1353a4785993a5a5a4e585855d59e41af2e8`

```dockerfile
```

-	Layers:
	-	`sha256:a53f7f60e39717f7a0efecb3e128afd8ebed31d61f87f4c20eb2983400f27c6f`  
		Last Modified: Tue, 12 Nov 2024 08:03:12 GMT  
		Size: 589.1 KB (589067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c21ea7363c904e57084e8cb72b679242d019bcab34712ee7386fc996d3c94eb`  
		Last Modified: Tue, 12 Nov 2024 08:03:12 GMT  
		Size: 45.6 KB (45597 bytes)  
		MIME: application/vnd.in-toto+json
