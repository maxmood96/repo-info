## `postgres:14-alpine3.20`

```console
$ docker pull postgres@sha256:d139fb8e51c5b8738004a5707f620bcbcecc6f493960b91a35960d2038d322b8
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
$ docker pull postgres@sha256:f74e7dafc11817144b51143c1c43114d709421048d3e14cca2270ab7d9bf48c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95370608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5be9634f46f806441f630da74a1153a3e1c4ab977394a97cadcc3ffc2bb96a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=14
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=14.15
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=02e891e314b4e9ee24cbd78028dab7c73f9c1ba3e30835bcbef71fe220401fc5
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c4fcff392d7016897432cadb68139a23e3e4e4459989aae592625af562844b`  
		Last Modified: Wed, 08 Jan 2025 18:14:37 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bfe7d9df76c5147f987448f1b941bc2d483e910d5bbcbefe264c02015ae6d3`  
		Last Modified: Tue, 14 Jan 2025 20:38:53 GMT  
		Size: 1.1 MB (1120284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6220b8192ffe167514793e663dbe6a9c4c45077360701ee7c2352c278e1ed9f1`  
		Last Modified: Tue, 14 Jan 2025 20:38:52 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3db02c78f16e1831210e281d9e97f95d4d065c5024e6227445cf09279f1659`  
		Last Modified: Wed, 08 Jan 2025 18:14:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96fb640dd32c417dd323bc4fc1d068e058e6acd8c2823e2ebd495dcc407d2ae`  
		Last Modified: Wed, 08 Jan 2025 18:14:39 GMT  
		Size: 90.6 MB (90607680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cd4af9e8311c508e8570d849603da49c4b75f5cbdec3e9ed770e5120c86a10`  
		Last Modified: Tue, 14 Jan 2025 20:38:52 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a8baf3cd2258824a92b7b29ab7025a887b7371890801fc89db6e587e6a301f`  
		Last Modified: Tue, 14 Jan 2025 20:39:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574b9821b652bdbbc5d61bfce43ee33fee99dabef4c76320d0a8e26bbdc87bae`  
		Last Modified: Wed, 08 Jan 2025 18:14:38 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ec9bedd86cbaa182c857ba783a642c1b6b33d80015199b0e04c67a3de35cce`  
		Last Modified: Tue, 14 Jan 2025 20:38:57 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2992358bded51b28e94657eff8987a87062e99615bb06948706932b2c130400d`  
		Last Modified: Tue, 14 Jan 2025 20:38:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:56ede526f2293f5510358e55b0e54b9555b6e2c4ae2c087d5f5fc3b12327b375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 KB (634495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0d5998e89827fd6a98e163276ba98ccd2744de90c61fc852190e2dd35fcc80`

```dockerfile
```

-	Layers:
	-	`sha256:b68f2aa4cab427a5ba97a9b6d1186156f0ef8f157d94945c9300f5561aadd280`  
		Last Modified: Wed, 08 Jan 2025 18:14:37 GMT  
		Size: 589.5 KB (589526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5062d1572392bb3bb6bd36d3e48db7241cf86a1e9810678f8306c742a604f3ce`  
		Last Modified: Wed, 08 Jan 2025 18:14:37 GMT  
		Size: 45.0 KB (44969 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:fed38073871234eb08cce825255cf1ccf734856039ab5a532b1027b890f9ced7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94145401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65323f78bd9a227038fa5654cd60e17148a16eb428afb76c54ee240f9793c384`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=14
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=14.15
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=02e891e314b4e9ee24cbd78028dab7c73f9c1ba3e30835bcbef71fe220401fc5
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88efc830b0008c442fbf41800df30ca9fb0c00964fddd3e80890961627c5b9b8`  
		Last Modified: Wed, 08 Jan 2025 21:05:18 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0135973424a59bcd09d82651ba32d24eda2b75299b4d2e3f5deba54f7b2553`  
		Last Modified: Wed, 08 Jan 2025 21:05:18 GMT  
		Size: 1.1 MB (1086512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4b0d2c7f42b79dc01dbd3833f6c268867a01749968770c19b0a257a02954cf`  
		Last Modified: Wed, 08 Jan 2025 21:13:33 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b35d591cbe9900f8759fa3be037a5061e3b63755c2fd7f4c9e8ae8112697b1`  
		Last Modified: Wed, 08 Jan 2025 21:13:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ba5f2fa575d850959338d5bf02798c4385fc4fcbd75cc9f6f483a0c1b193bd`  
		Last Modified: Wed, 08 Jan 2025 21:29:36 GMT  
		Size: 89.7 MB (89671034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db36ee424085c2088b6f2655cf500cf1431f9ae5d9cfb415fb7747dc38b23ecc`  
		Last Modified: Wed, 08 Jan 2025 21:29:33 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c114463bb432f33ac1668ae6def43ec144020c5a990eebc5defdff2ebdc7f7e9`  
		Last Modified: Wed, 15 Jan 2025 05:05:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be706a54a219a8f19c9514f68b8539ba48862cce36741b7885fd5d5c46123f0`  
		Last Modified: Wed, 15 Jan 2025 05:05:34 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8877578bc0321d9ca4c71067179e20253ad96d4900099cf03c1682b109bbca85`  
		Last Modified: Wed, 08 Jan 2025 21:29:34 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f492b3d55c1a09a32f4b54deede6b9057091b9299e03585a42ba64addd7398b8`  
		Last Modified: Wed, 08 Jan 2025 21:29:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:8fd82a8b53a769a6024cba89dbc31b1d4a8bb42af41976e6be9b26747b39bc8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 KB (44918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a5e609cae11faa8d5c9d7f16471c47f354f5101d9b4097a633c4ddd9fee261`

```dockerfile
```

-	Layers:
	-	`sha256:4a4fa1b7be0386a3f567bda85be2d1ea359d8a045e496b19280b49fcdb1059ba`  
		Last Modified: Wed, 08 Jan 2025 21:29:33 GMT  
		Size: 44.9 KB (44918 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:2feb9f6ef739e9f66f733434444cebc29b692c20ae65b6c7c32bf92b1101deb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88581379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b379eee0ec7f48c323f3a4f7ec01175096bd59f3907a89263aa78f715573135d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=14
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=14.15
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=02e891e314b4e9ee24cbd78028dab7c73f9c1ba3e30835bcbef71fe220401fc5
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Wed, 08 Jan 2025 17:34:15 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b746070b0d0b0e37202f22f09fce21559849b7cfc62d09b1ccc2c4d324ce4b88`  
		Last Modified: Wed, 08 Jan 2025 21:11:35 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af679bfaf56ffe9fecae43f4b7f02611bb9b4a9d9be36b50592229008b20fc0`  
		Last Modified: Wed, 08 Jan 2025 21:11:35 GMT  
		Size: 1.1 MB (1086516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a574428493c8bb9e03f453f358c30456195031ee6dc5fdbcd31eb4c12324e1dc`  
		Last Modified: Wed, 08 Jan 2025 21:19:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbe265cd4c437408918c4e836299d627a0ce5979cbf59cc33e9bab1e3dd6262`  
		Last Modified: Wed, 08 Jan 2025 21:19:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37db1153c6e07dd3d731b9ee7740c8051e41634162407bcdcc2768d6734f4aca`  
		Last Modified: Wed, 08 Jan 2025 21:35:31 GMT  
		Size: 84.4 MB (84382964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd46f923afe4b2c97e5387a7145e08bbf0d638255ff0759c0eb29772af03608`  
		Last Modified: Wed, 15 Jan 2025 05:04:49 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab3aaf3e8c0015161d3e83bbff7964cc7b4a0555fab3272964dff2d41e2f3a9`  
		Last Modified: Wed, 08 Jan 2025 21:35:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6868c70696e0d3d01f0966a5cb46c0ba25f8991d17684a66576d5badd4423b`  
		Last Modified: Wed, 08 Jan 2025 21:35:29 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d836e3da9284dcd53ce5306ee09b206c6104cd0632761f86419b26ec4cd66357`  
		Last Modified: Wed, 15 Jan 2025 05:04:40 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92593ff25dc865629fafb234ebc51a074f62032f1c4a8561101fbfd59a38a811`  
		Last Modified: Wed, 08 Jan 2025 21:35:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:18b6317ca2d637b6f682fe13bce5f5183764cb3789310ab7e34a6113453447a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.7 KB (634679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116c7ec64064b40f3dd78cba45655311a6461d2ca3f22ec9a09fbea9abeb10d7`

```dockerfile
```

-	Layers:
	-	`sha256:9b7e0219af3419c27d8caae6a827d18fd7101fefbf173a9bb6e053dc4201953b`  
		Last Modified: Wed, 08 Jan 2025 21:35:29 GMT  
		Size: 589.5 KB (589546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef9a3e62b352ed95dfb06340e84b959bf9c9cd2ff84eafae4c6872333828a11a`  
		Last Modified: Wed, 08 Jan 2025 21:35:29 GMT  
		Size: 45.1 KB (45133 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:0619770c10a2042699528561d293c54d7eaa515cce84f3b7ff431b3e1c7f9e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94620713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03dc4c7119c12ed2c01e95c3090be107a9816887e0fbe275b25ae426c21e2889`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=14
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=14.15
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=02e891e314b4e9ee24cbd78028dab7c73f9c1ba3e30835bcbef71fe220401fc5
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d44399ea45a930603df43b60dc9b107535c6cf565758aadbb124b0eec4bee00`  
		Last Modified: Tue, 14 Jan 2025 21:58:35 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad7be62d19dbe32494df2ba4a737e440946b4a8373c47d5a600dba48ed6adab`  
		Last Modified: Wed, 08 Jan 2025 21:23:45 GMT  
		Size: 1.0 MB (1049757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25a5092df8e17dac09425f12b17a14dedd5d271ab884d779a0a9b5116c6f7d5`  
		Last Modified: Wed, 08 Jan 2025 21:29:35 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0ce2df9d0312a11aac7fa86527a4967d9ccf652813cfe5cac4d3d08b1d887f`  
		Last Modified: Tue, 14 Jan 2025 22:12:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6c08c9fa5f7d473d5da107de4c133f039a4e7e846f2b8fec9022e73ffe7d48`  
		Last Modified: Wed, 15 Jan 2025 05:04:02 GMT  
		Size: 89.5 MB (89463811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256377e5705e6ecc0da1ffdab5d3ef6daf78587286d2372e34c0c20ef4d54c35`  
		Last Modified: Wed, 08 Jan 2025 21:40:49 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbf394d45f03f937cead92aa0c51c1aaa0c87d724d81e044246859dbade1738`  
		Last Modified: Wed, 08 Jan 2025 21:40:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4849db98b4cb37c6caf925910bf1c09a0e88501e1056301325c3d893be229803`  
		Last Modified: Tue, 14 Jan 2025 23:56:46 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da59ec901cbcf05618c225e080d65d61d442dfab4ddc0aacfb02ecfd41e2ddbf`  
		Last Modified: Wed, 08 Jan 2025 21:40:50 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709fc510fc3bf4a4384dd3f083f7beb2c6f032f3fe48249d31adca66adc49562`  
		Last Modified: Wed, 15 Jan 2025 05:03:35 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:433638d08d38b16a946e65bb8063cad7c403fe05299a09fa1027f2eff58fe43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.7 KB (634726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a29e484ea44dfa65fb098e3e2b6f4878e9259ced718896ac02083997463fc15`

```dockerfile
```

-	Layers:
	-	`sha256:94f9ced5bababd9e90452eb6aa67fc79ad7a33cc2e26eb8606512663328222dd`  
		Last Modified: Wed, 15 Jan 2025 05:03:27 GMT  
		Size: 589.6 KB (589558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:324e9fd293d70fa909079c3dd1e8dc4e6f5de1d051783c06766a4ad96408dc0e`  
		Last Modified: Wed, 08 Jan 2025 21:40:49 GMT  
		Size: 45.2 KB (45168 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:31fff7ed636a1533b9483607f4cba49703da39d159d22385dbd6884390c2101c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100684488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92fa024c367c2421b0d56c98de86ce0d975c4e9c4cc73234fd5c68dc43a39b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=14
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=14.15
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=02e891e314b4e9ee24cbd78028dab7c73f9c1ba3e30835bcbef71fe220401fc5
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6e17bf3ad0290134f2d542f455c986dbfc9e8c9d0f2eec1076ba0ce8e9d167`  
		Last Modified: Wed, 08 Jan 2025 18:10:31 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73afc5ec0607c065e40546882fbdeca76642ea551d955bd14efddd5b7069d71f`  
		Last Modified: Wed, 15 Jan 2025 05:03:11 GMT  
		Size: 1.1 MB (1095374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e9c09eb3fc04ac80fbd9ddc6097ea2e1ced9febe816faaedbe722cc0c1ff52`  
		Last Modified: Wed, 08 Jan 2025 18:10:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ef0b393ed7fd083df32a1375248e8a9083a8ee22d8a0da13dd95c31e4852c5`  
		Last Modified: Wed, 15 Jan 2025 05:03:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c3eee55a8680f52b96625b710cc07bd547dc2df4844fb9be4cc3cd65a921df`  
		Last Modified: Wed, 08 Jan 2025 18:10:34 GMT  
		Size: 96.1 MB (96101769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e436de4ab99bccd07acdab00bd1f10444fa796110bdc47aecbc05796ce9faab`  
		Last Modified: Wed, 08 Jan 2025 18:10:32 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d860a7c5c23b5b2e1a897f9d72f6701a3b70fefd00459ed42a13a63bf4dac3`  
		Last Modified: Wed, 08 Jan 2025 18:10:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1d9f83934400ce4051c7f335a136e213bde88ee9ae95bbbb98e37bb84aa654`  
		Last Modified: Wed, 15 Jan 2025 05:02:35 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8b4a1b9c71fe92f9fe56a8d6a216bd07db2f659e51fd5a6cf402e4ea316c1d`  
		Last Modified: Wed, 08 Jan 2025 18:10:33 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e44bf2903e5578010130fe4a80438589d763c4bf8b4590178ae69a58bf95e2`  
		Last Modified: Wed, 15 Jan 2025 05:02:28 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:b906419228c03f6d84a51bb283ff89e45d995f106c1c18a4ebea26355c076aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.4 KB (634442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990eaea688079efe2d7e82c4397da7bb30b71f05adacfae5dc019f4ae2d33f7e`

```dockerfile
```

-	Layers:
	-	`sha256:d4901b6e89ff2264e29f38137767ac0e2552da67449d921fcba58a73b9391479`  
		Last Modified: Wed, 15 Jan 2025 05:02:18 GMT  
		Size: 589.5 KB (589511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8161b3c28458a476b552bad3eae5a210301024ff36c0fb14b42f3f30bc8f54b6`  
		Last Modified: Wed, 15 Jan 2025 05:02:13 GMT  
		Size: 44.9 KB (44931 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:e37ff5f4af6de3b70ceceda56a0f286ee6b3438c3e5d41b1e32ba76c897bec91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99878077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba990611dc0391e9ecd28b663391b073dc736cba08fc874e53a35057d251030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=14
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=14.15
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=02e891e314b4e9ee24cbd78028dab7c73f9c1ba3e30835bcbef71fe220401fc5
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd99b41e4eab97b8e99f151e356a73dcfdc6852319a226acefd789ac0a0fcdf6`  
		Last Modified: Wed, 08 Jan 2025 20:47:42 GMT  
		Size: 987.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01865a7aee85aee7eba24c5081ddf5c11e292c121e446bf7b6b6e679c5942374`  
		Last Modified: Wed, 08 Jan 2025 20:47:42 GMT  
		Size: 1.0 MB (1040020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98e8a6ccc51b487067716d0bf747e8eb0136bc2b9de2616369fb010565bff1f`  
		Last Modified: Wed, 08 Jan 2025 20:54:43 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b122119b1a97526cadfe6c461352381002a72b1f72b568d10edb1e12f012fc`  
		Last Modified: Wed, 08 Jan 2025 20:54:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6090b211498a82b9d0bca94de8611b361ceccf3e764920976d927de729967261`  
		Last Modified: Wed, 15 Jan 2025 05:01:54 GMT  
		Size: 95.2 MB (95247266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0595b7641b0553a9e5dedb0c41888636c58279cb3b359890b539af116fb5261f`  
		Last Modified: Wed, 15 Jan 2025 05:01:41 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf18425ebe53006bc3d99d55fcf3f9b280fc7fe7e0f97901fb72652dd15ab820`  
		Last Modified: Wed, 15 Jan 2025 05:01:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c60d000e9a3d95408e27e1486fbcd807922ac6ed2acd76e117a5b73b4e02aaf`  
		Last Modified: Wed, 08 Jan 2025 21:08:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1882c61e93c597baec7f683fea512b1c14df5e8bb6803b96bd15df145926870`  
		Last Modified: Wed, 15 Jan 2025 05:01:27 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fadd13f3cadb7ab7d2562cfe919544374c75853d39066dea9445e8f3aefcc0`  
		Last Modified: Wed, 15 Jan 2025 05:01:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:3671570d40c72e3347b1ad14919df6d3081392e4fb6c4a64ff3d3729ce7e920e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.0 KB (630952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19c34392a6d038fc6816a8892a56fec76512b6f2a82552a5728bf957103eea8`

```dockerfile
```

-	Layers:
	-	`sha256:6242b3d51b464ebfdd3a64c05f99f95821e38321c75f2e78c4275938b92f6a41`  
		Last Modified: Wed, 08 Jan 2025 21:08:40 GMT  
		Size: 585.9 KB (585935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9fc5a9c90216975f68c18b3b135cecb3f606179580066667db395dd0c765d13`  
		Last Modified: Wed, 08 Jan 2025 21:08:40 GMT  
		Size: 45.0 KB (45017 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.20` - linux; riscv64

```console
$ docker pull postgres@sha256:1cbdea8fcdbb2702edaf5d6b18d575b1ecf5a480fa1d228a06b1f0f5e17868ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95505617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82416ed78efc874d841279b111f0a911df5f552d76266b31405ee1425da85f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=14
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=14.15
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=02e891e314b4e9ee24cbd78028dab7c73f9c1ba3e30835bcbef71fe220401fc5
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Tue, 14 Jan 2025 20:50:16 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc93498547eda47632be52e4f9de0f535264be6b5b13bd695df74d21a445ee4`  
		Last Modified: Fri, 10 Jan 2025 08:04:23 GMT  
		Size: 988.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4379025cfe409827e83762b8ddf18bccb050a044fa62c5ba40f88f35ee905545`  
		Last Modified: Fri, 10 Jan 2025 08:04:23 GMT  
		Size: 1.1 MB (1089578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef0186356e321fef013e99e866a37e8308d9f788f5c47123b149b521575eec0`  
		Last Modified: Fri, 10 Jan 2025 09:45:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24206bd7240c9a3da106ad9224c974a577cee2bb13977c8f2b4de67741d06e77`  
		Last Modified: Fri, 10 Jan 2025 09:45:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a35032c25653d3395b30b513738caf2fc6c6e96002c0ad35b436da68c6171ec`  
		Last Modified: Wed, 15 Jan 2025 05:00:56 GMT  
		Size: 91.0 MB (91027727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d93729a9033bc1febed08f4cbe0d96d836d843f192525f3745029e07ae9af14`  
		Last Modified: Fri, 10 Jan 2025 12:32:02 GMT  
		Size: 9.2 KB (9208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696e8559e2f3b03ccefec318a63c2cbf755590f5404bc1362d0cbca50fe97e2f`  
		Last Modified: Fri, 10 Jan 2025 12:32:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6d768da6a11e21c2e179f193e394b6676a135f20982676c664da2334bde94a`  
		Last Modified: Fri, 10 Jan 2025 12:32:02 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a74c2d5d8b2ad75bd7ca66e4dfe46a9d38cb9a3282aa6fd837d93939386b013`  
		Last Modified: Fri, 10 Jan 2025 12:32:03 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be422d076b2b9bf9a47c6cfd10d23601827644bda39f646e2a8ac604bca10fb2`  
		Last Modified: Fri, 10 Jan 2025 12:32:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:dcf2a2ae3a7b8f5416ba4381f3f58060eccf1a8ea6197a2ffff4df4828b03314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.6 KB (632608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b11c5e7debcae36a2362a7fce18d49729566d1852d84c3b58b1992318ab8a2d`

```dockerfile
```

-	Layers:
	-	`sha256:b3103fd8b0a3a8ea48db357638eee300e539095e90b624a4b9420e362f055613`  
		Last Modified: Wed, 15 Jan 2025 05:00:21 GMT  
		Size: 587.6 KB (587593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11c79b9207045936a9af0ea7f006273aa1ffb47d10fbd46e46b473f5d7b664a1`  
		Last Modified: Wed, 15 Jan 2025 05:00:17 GMT  
		Size: 45.0 KB (45015 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.20` - linux; s390x

```console
$ docker pull postgres@sha256:199457ced3caf41cf2c7a86ec8886c103fcbacb60ef5461f2b9a97671c5ef511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104262095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c30844c806efb1961ab7aaa28ff4226e260596881d4a0adf5029f15dde859b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=14
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=14.15
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=02e891e314b4e9ee24cbd78028dab7c73f9c1ba3e30835bcbef71fe220401fc5
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Dec 2024 00:14:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Dec 2024 00:14:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
STOPSIGNAL SIGINT
# Fri, 06 Dec 2024 00:14:30 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Dec 2024 00:14:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dc2876242de6bd7252b9ba2b4d53f4eb9fbcecfa1d99a33799aac75fa77090`  
		Last Modified: Wed, 08 Jan 2025 21:22:54 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864521ac5f08c5acac350319254a85153aba704edfa918f1373f4d3379e84be2`  
		Last Modified: Wed, 08 Jan 2025 21:22:54 GMT  
		Size: 1.1 MB (1084151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af466fe88aee254e0f612f2229ea0019a6fa590b2b240af14f886dc47d9b4d82`  
		Last Modified: Wed, 08 Jan 2025 21:30:40 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51451cadd271577a382834a257c7920101534a8811c78d1f30f05e05575cbf25`  
		Last Modified: Wed, 08 Jan 2025 21:30:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92c65f0cc59ff060f9fc939860e815931907f208e37dbfc57625d497e01cd24`  
		Last Modified: Wed, 15 Jan 2025 05:00:00 GMT  
		Size: 99.7 MB (99698244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff237dd5098733dc341c8f920bc81087a8412b8dbd22db5b750cae049770193`  
		Last Modified: Wed, 15 Jan 2025 04:59:48 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181b72cbd441735bf46a3fd89ccf9e3da79909cdf73a6a53c5fa5031b07a23c1`  
		Last Modified: Wed, 08 Jan 2025 21:45:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9b245b4bf1a470af883c81b98c0de2807348e34e504089ff52b59c8baedc2e`  
		Last Modified: Wed, 08 Jan 2025 21:45:49 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c36239ef43e4ecbf67cf94d86dff4f90fae2a23845dcac40644fda1886c987`  
		Last Modified: Wed, 08 Jan 2025 21:45:50 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d527c05bbc78448eec822a470a03872f2b5ae2c702d1e09cd1902216217da901`  
		Last Modified: Wed, 15 Jan 2025 04:59:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:52ce36955cc0a193c278a9ba4c2b5281a56f86ce7863563551aa9c98a2fad6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.5 KB (632544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad323e40c787ea004675d1f8c815608c3ed798fba3f874a2a9d44ca7d5232664`

```dockerfile
```

-	Layers:
	-	`sha256:52120bb91e9329d681837979491582fbba30ca4ee0dda2b188dacda0a408cc4c`  
		Last Modified: Wed, 08 Jan 2025 21:45:49 GMT  
		Size: 587.6 KB (587575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7890e6cc0fdba04bcb8e1f014e9ed45322712ba6b0144a0830eed3023cea2ea`  
		Last Modified: Wed, 08 Jan 2025 21:45:49 GMT  
		Size: 45.0 KB (44969 bytes)  
		MIME: application/vnd.in-toto+json
