## `postgres:15-alpine3.20`

```console
$ docker pull postgres@sha256:94ccd2556193659e29f2476c09587649edfd146c5b02c6cdeb9a8dc4b0437a97
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

### `postgres:15-alpine3.20` - linux; amd64

```console
$ docker pull postgres@sha256:041520572f419a40917066130690c9bafedb1a553ea1e189d9a3b8d62a6b50bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96014264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fe5c03edce8d3e02fc5e295485830b4e3c23e14f919c650050c3510590c2ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
ENV PG_MAJOR=15
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=15.10
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=55abe738d441f0e58658b3ec6f88097a713b5e3b73139f6230d7b5c4c389e573
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85de02dab8aac3760d0b06e2c32b790b58caea227cad97afa99c6975ffef8124`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c625b51b0cfc3e7cc057d09ee3818a3da3e83ec2588d0fb3ba350d88d6f66f2`  
		Size: 1.1 MB (1112181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e974a90add5f9804aea59a8e4bbb795c5dfb36e19eb7c44f7e605c2497a31120`  
		Last Modified: Wed, 08 Jan 2025 05:56:05 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032744de550cd78074da254b725ce9bc72b65b4b4454a52e8675af5591207b95`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e8e25ef447065ec1bd30c068a3bc85c79ad9ead34071868b275535a96db331`  
		Last Modified: Tue, 07 Jan 2025 03:32:47 GMT  
		Size: 91.3 MB (91271465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ffa4f67e2d79e7fbe60078afab9b5e8a733f34142b21e87da5e549db859dbd`  
		Last Modified: Tue, 07 Jan 2025 03:32:44 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf45d4b291cad2ab50008d67023ae1c4722681ba31c2d7a738cf1440c4513e5`  
		Last Modified: Tue, 07 Jan 2025 03:32:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a7a541859516b624348a4d3f233a792d57218b90185190fb1244c56a8fd270`  
		Last Modified: Tue, 07 Jan 2025 03:32:44 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1777bebc73a2746444fe23c89af5dfa5220b759445ce84d87b5cb44b0590c5cc`  
		Last Modified: Tue, 07 Jan 2025 03:32:45 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce74ee22718d8461d783483ae1a3c7bfc937a8a1de3b66280794eadcc3d0382`  
		Last Modified: Tue, 07 Jan 2025 03:32:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:425af6f5e66544fabb28efa5dc813aa883f2bb39be658b56cb2e5cc23cf0966b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.8 KB (634814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff49462903b5c797f33dc48f7c3238ff0f874490807b33dc03052b9d40b92efe`

```dockerfile
```

-	Layers:
	-	`sha256:5c568c2f2faa5fe455c0f0ae41cc2447b1a943fc6cff9e71754bb07717619faf`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 589.5 KB (589526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a23264ab30627d8213d96bd8e904390ee4fb6ccd16f93e4e2934450964e5a411`  
		Last Modified: Tue, 07 Jan 2025 03:32:43 GMT  
		Size: 45.3 KB (45288 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; arm variant v6

```console
$ docker pull postgres@sha256:bed0823e7b59a3cf7206e077dd90db54f9b8284c1860526e8098f4a9f37cf717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94785421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680d87b0cdfb46f1be905c533c7405afb4175f854b847daaeaeec8e9de40cdb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
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
ENV PG_MAJOR=15
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=15.10
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=55abe738d441f0e58658b3ec6f88097a713b5e3b73139f6230d7b5c4c389e573
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f478230af6d9a94a10f9570d33e7e450b7aaa5d99ee75790a082536a62884cea`  
		Size: 982.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ef499b999bbc83f320da62c82914be5640edf1a6fd8a16ae7a32efec59f30a`  
		Last Modified: Tue, 07 Jan 2025 19:38:29 GMT  
		Size: 1.1 MB (1081695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848556d69738a6c7c47b7d1d541aefee0f0958f94e30700970f0d59323351270`  
		Last Modified: Tue, 07 Jan 2025 19:46:29 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2468d5c1b605eea3499af8e185ca84ca772833d808f71942a8501e62ff5f192a`  
		Last Modified: Tue, 07 Jan 2025 19:46:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d03333a3b0cbf24600a5e21c34f5c9cc3972d583f5a1d6b665e897d401ad06`  
		Last Modified: Tue, 07 Jan 2025 19:53:35 GMT  
		Size: 90.3 MB (90323161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8702cc8ff0acb69f36245693a37dbf33388fae1de115ea335727cde6bf4d9e`  
		Last Modified: Tue, 07 Jan 2025 19:53:32 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73be377b8faf1369acf2967f2dd47ab551334f29326847208b4bb342d48011a5`  
		Last Modified: Tue, 07 Jan 2025 19:53:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f2622a3676f2e96ae0b8e9825955a078f6c4755175e774238637c1f64cf976`  
		Last Modified: Tue, 07 Jan 2025 19:53:32 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac39288eb7d88777a8f4dac636471abc4744807a992ca2754a5f52902135df1`  
		Last Modified: Tue, 07 Jan 2025 19:53:33 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b32a7ce1f172e92060a4906dba94ec08e048c6ce478a97fdf17fefb48b71d4`  
		Last Modified: Tue, 07 Jan 2025 19:53:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:fc02b32127f44340c3b72f67f2da8f2c79f166ba00270ba3bb1327e30a8afb58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 KB (45237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50278409c2338213100ffede7ac9e34ca45ecc5284ae4bb874d1a2c075400e6`

```dockerfile
```

-	Layers:
	-	`sha256:e340d8f0d0ae02a1f3ba685fb568ef6d15f1db87c24aef223a7335b9c88b3032`  
		Last Modified: Tue, 07 Jan 2025 19:53:32 GMT  
		Size: 45.2 KB (45237 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; arm variant v7

```console
$ docker pull postgres@sha256:ed989440b59cfd0e647a7290c1cfa0233efd7d5a5931a13668b13f1bf67662e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89211254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f615696d3c0a7bd4a25d163c2a9854481eebfe7b1158b0827089dae6e685fdb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
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
ENV PG_MAJOR=15
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=15.10
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=55abe738d441f0e58658b3ec6f88097a713b5e3b73139f6230d7b5c4c389e573
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d274efdde52d0ab421ade1b32d0d5f2b4fd5f03fb29bb2577412091f37a9c3`  
		Last Modified: Tue, 07 Jan 2025 20:06:47 GMT  
		Size: 982.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b670c58a083a6a1d32b162206398a53fa8da33b059ea514297ba9c55572da5`  
		Last Modified: Tue, 07 Jan 2025 20:06:47 GMT  
		Size: 1.1 MB (1081715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1de66c83343bcb368c7174b72f16e49c7c1b9f1cc29cad6c6838bcaf787aa2`  
		Last Modified: Tue, 07 Jan 2025 20:15:25 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782c763d21adff94e45ea91f07059701f6aeba11fa815beafb3b0925cceae40f`  
		Last Modified: Tue, 07 Jan 2025 20:15:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61871dbd58bab7a51fdb44ad490a5c7697c6ad3a4c01cd4731218d944e5f890`  
		Last Modified: Tue, 07 Jan 2025 20:47:24 GMT  
		Size: 85.0 MB (85021642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64176bb6bd70a297226d72f3893bb51132878243a6b1d0242e7ff797f67e207`  
		Last Modified: Tue, 07 Jan 2025 20:47:21 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f2f36bf612d8e00f48b3630ed695ffdc3ab8bdc22cd300eea1eff889da6b6b`  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa2ae2b3a3887daca39b3477d887479deba47079c3fbd4a2dafc3671f82a516`  
		Last Modified: Tue, 07 Jan 2025 20:47:22 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777795249c2ea1e049730bc60a4090274b62bcc43abb3d8677e81af0dd5e5181`  
		Last Modified: Tue, 07 Jan 2025 20:47:22 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d40b7826953d44c6d05f2f6c3826d0d3ddbd468bce7973494246d780ef91ad`  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:bb4967897d9662843add57b962c8b7e04afca01a64ea15a70ce52dfcdd66b57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.0 KB (634998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c6c05f3f61f779fa1fa23e9dbb87c60b6d2f138e0a26544255694093e494af`

```dockerfile
```

-	Layers:
	-	`sha256:765b9c69365ffa7eb4b5ff8ef37266764506236ad3c12fdfa6defcdc50ff5aaa`  
		Size: 589.5 KB (589546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd132fc0d02742e0c9f2bb39daa85281b41f856f69fdc1164bae34c73a6294d3`  
		Last Modified: Tue, 07 Jan 2025 20:47:21 GMT  
		Size: 45.5 KB (45452 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:286ea98ce072bfe1e484fde27045ee559291b7f1f924d419ec81b2b619f156fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95261923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b8f6c26edb91294e7ea7757387cc7acfa6aa6db3dbf74f1adee2622ecf50b4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
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
ENV PG_MAJOR=15
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=15.10
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=55abe738d441f0e58658b3ec6f88097a713b5e3b73139f6230d7b5c4c389e573
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb18ebde9da6b7ef62116ff01795eee1d1db364a53f6603825008816862bb13`  
		Last Modified: Wed, 08 Jan 2025 05:51:54 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbf648fab39a14d56d2995aa02eeccb5798032d03567e2a1e2c6be79cebfe71`  
		Last Modified: Tue, 07 Jan 2025 17:54:08 GMT  
		Size: 1.0 MB (1041708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89e0b018b26a7fc8073902d407a3dce1b6453138a08aaeb8139f7acf3d25cc3`  
		Last Modified: Tue, 07 Jan 2025 18:00:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9dfb0f46059b8df8d64763a5fac060ae49d7445ee982c9c8605de84c2eec4f2`  
		Last Modified: Tue, 07 Jan 2025 18:00:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86af4e6e7491dc5736a2eafb878e69cd45bc414eea38a93c205263ff9024a7f`  
		Last Modified: Tue, 07 Jan 2025 18:06:21 GMT  
		Size: 90.1 MB (90116901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef1a389350dc11c471ac92bca912411b3895e37d661530cd247ac3b908db0b5`  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bef66bf78325c06b7de5f77b06b18e62060cbf0c31ad670d29e0e43dc548a6f`  
		Last Modified: Tue, 07 Jan 2025 18:06:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cb43b21aa334dab79af7a695272d6866f48c87079ea5d28f23410633d17b90`  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f0c50d74cf0e3f5074fcbaba814c953430e03a3515f6406b77d3997e22dfe6`  
		Last Modified: Tue, 07 Jan 2025 18:06:19 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca52f01c86980b856b8933dacb74d785653c4dcc896add346d1e3c1dcd2a50e`  
		Last Modified: Tue, 07 Jan 2025 18:06:19 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:437fd84289c28774570a823f80c1766d7fb78264bc5722311cbb5a6cfa9f6d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.0 KB (635046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350c90ab8e45cb5c4e0e158016ed3a16160a991049b2d45b7c95ed95892919dc`

```dockerfile
```

-	Layers:
	-	`sha256:5199aa1c4061af88ebcb5b5071ac78f544bc8c1aeb9a4cce205f4857a0a19abf`  
		Last Modified: Tue, 07 Jan 2025 18:06:18 GMT  
		Size: 589.6 KB (589558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e86c567ec48db54df9d42cbada5f6c5c10de2e51e875fcd6ea254af7c77835d`  
		Last Modified: Tue, 07 Jan 2025 18:06:18 GMT  
		Size: 45.5 KB (45488 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; 386

```console
$ docker pull postgres@sha256:d5ff3501c418b3231b42bb01eeaf104146adbe85ffa1eea6b6c2c7883c8d8703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101364721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edb0cd6ec93b9b699cceb658a96903e7cf9fe0a3402bfc3d6e7a30b3e5b6a3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
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
ENV PG_MAJOR=15
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=15.10
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=55abe738d441f0e58658b3ec6f88097a713b5e3b73139f6230d7b5c4c389e573
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34612e614c78712a121e4ebffcdb45c469b06a1e6097867c27992c55ae71138d`  
		Last Modified: Tue, 07 Jan 2025 03:33:10 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6cfe4fc634ba6c0d9499bc789a6385d90aecc304931f0967b24cb9313ecf11`  
		Last Modified: Tue, 07 Jan 2025 03:33:10 GMT  
		Size: 1.1 MB (1089420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae20724a750d1149230b01f4d690eb009c2d4096de3366d275b9f2b98580013b`  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fe902edf80f10736d00fc328ba29b7c5d556daf873be996465f9dbe639a3c3`  
		Last Modified: Tue, 07 Jan 2025 03:33:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb610db4ff55108ddda29dce457da029ef0e8d596a49d2abaccdd22c3b41a2cd`  
		Last Modified: Tue, 07 Jan 2025 03:33:13 GMT  
		Size: 96.8 MB (96795494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834be91795dc9353c0bd824a28736249e7e36ac6cdacf6b836260968d72808f3`  
		Last Modified: Tue, 07 Jan 2025 03:33:11 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4dcf5ed80c0c52485088a8d99036a0cb2930227df51f66a1cd3f2e473bee1f`  
		Last Modified: Tue, 07 Jan 2025 03:33:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5c2db0c7ec9bc483fa2587041e3680d244166167d84db5bfbe67b16b1356c5`  
		Last Modified: Tue, 07 Jan 2025 03:33:11 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b324036d1e18fa715ae70b2822a860ee06c2fb3fa75cd41fa7735fb4fcd617`  
		Last Modified: Tue, 07 Jan 2025 03:33:11 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11cfa6a973992f438c58cfa8f07b5527e3278d4779dd4c625ce87e8d17257fed`  
		Last Modified: Tue, 07 Jan 2025 03:33:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:255a3ff78f250f3240421a3eb4ccbd22c1605788247ea964421b05d6d082be79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.8 KB (634761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c714f8c4b73aa516bfbaa020ed7b3b3e30e8a93a87323cb73b1bc275538b6a80`

```dockerfile
```

-	Layers:
	-	`sha256:00f901fbdf56dab2372e0ac9060fca0f22ed86ded451845d27a4b9df18e22ef2`  
		Last Modified: Tue, 07 Jan 2025 03:33:10 GMT  
		Size: 589.5 KB (589511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44d78c95335a195b67a8f7013d95452d669f330d45e26cb5effc44037c4e0607`  
		Last Modified: Tue, 07 Jan 2025 03:33:10 GMT  
		Size: 45.2 KB (45250 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; ppc64le

```console
$ docker pull postgres@sha256:e1326278da1b698b72a56e066afa6071a1d74fee2794e1b4da71f22c8517410e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100574298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e3ee127bdb6063326ef57bb43d5199b42589546a4235af024f6b2dc439c3bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.4-ppc64le.tar.gz / # buildkit
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
ENV PG_MAJOR=15
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=15.10
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=55abe738d441f0e58658b3ec6f88097a713b5e3b73139f6230d7b5c4c389e573
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:c96bc34ea0111931eae2007b7db67b205ebd3c8a096d711e1be59e48f25006a3`  
		Last Modified: Tue, 07 Jan 2025 02:32:24 GMT  
		Size: 3.6 MB (3568727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b665d62410e208c4d22fcbdcac512c0f4ffca6f114f02f16f39d5fb2604f47d`  
		Last Modified: Tue, 07 Jan 2025 15:15:58 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7a6be0c58d18f750c63949c53c7e3a9539bd63442fdbb665ce390fdacb7384`  
		Size: 1.0 MB (1029821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7181fd99157faafb29e7d1703a5dbc83b3fe7c77224c92d77c8171d814b4ce93`  
		Last Modified: Tue, 07 Jan 2025 15:15:58 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0747236fd3eb97a0738ef4083b7577291a48915d135444dc7fbcec63926591`  
		Last Modified: Tue, 07 Jan 2025 15:15:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36d83c74ed233d1ee3527b6c4f63a48fa61b601729e175ff34e335106eaaa9e`  
		Last Modified: Tue, 07 Jan 2025 15:23:06 GMT  
		Size: 96.0 MB (95959128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d61cd67b8b559f4271606fd7fe5221236e79fa72cf0ab6b65030cc4e1effafe`  
		Last Modified: Tue, 07 Jan 2025 15:23:02 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74358f424d1d1a98c70c9cf5d595ace6580b27c4895e6b72cd43c0950518518e`  
		Last Modified: Tue, 07 Jan 2025 15:23:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b8f444ecdc7a2b72138c9abf7be7cbaeee8df1dd0bf6c96fb47b103a29f313`  
		Last Modified: Tue, 07 Jan 2025 15:23:03 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c9830938fc7448d46596eb374db30b24b7590c474dae36be1218b140b66b55`  
		Last Modified: Tue, 07 Jan 2025 15:23:03 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a541151dfa3d6975e378c0d7c251f0da9bde26251ae7f1a3894f119e09e586`  
		Last Modified: Tue, 07 Jan 2025 15:23:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:05aa49c0593b5c8defa4d731e3c22e3b4e4c9d070220cf6265b925a0b07ded88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.3 KB (631271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1cbd0b986dbff4ceb5f4098007f3aaadd4149ae4f322dc1f0f7f806a2cc8c0`

```dockerfile
```

-	Layers:
	-	`sha256:cf98eedd0a584587280e3327e4aa75377bf03b66deda68e515b69708725d8193`  
		Last Modified: Tue, 07 Jan 2025 15:23:02 GMT  
		Size: 585.9 KB (585935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e18eaaf4b7c8f3ac9b79a81183dba223cb346afe7a07933d5df2435d96640b`  
		Last Modified: Tue, 07 Jan 2025 15:23:03 GMT  
		Size: 45.3 KB (45336 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; riscv64

```console
$ docker pull postgres@sha256:cfea45321d2fac6b73f6bcc786e3417079b4d310d843061dc6fcbf98f0ae1e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98099359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adea381295d8a27f030ae9e94cba7f8a8d5ab5f892e9fd0d3277de47ed6a445c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
ENV PG_MAJOR=15
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=15.10
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=55abe738d441f0e58658b3ec6f88097a713b5e3b73139f6230d7b5c4c389e573
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8f6d509c68c45b1fdf0a1a4ab907f53741b31f985f51c20dc23cd8a8d6f8c6`  
		Last Modified: Tue, 12 Nov 2024 20:47:45 GMT  
		Size: 989.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38504f2cb255ba8a48a6b356aaff81feb5626bcddc945bbd59e7de7b2cbad90a`  
		Last Modified: Tue, 12 Nov 2024 20:47:45 GMT  
		Size: 1.1 MB (1087949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e6b162445bb1f4714c82ba5ee78e748e64dab99e6d2b388464c3cc9685b39d`  
		Last Modified: Tue, 12 Nov 2024 21:35:14 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71780435e839b7381f0d933d50d5f447819a9afaac78fd20e751316b070c6534`  
		Last Modified: Tue, 12 Nov 2024 21:35:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627c696c76c003e57055d6580b15db16a811ebce07c87da1243442c930d016a1`  
		Size: 93.6 MB (93623284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb48951a85bc66b4084ba5b8bdde8f33ef42a6d6c3120f8c79383da39e54860`  
		Last Modified: Fri, 22 Nov 2024 23:02:31 GMT  
		Size: 9.5 KB (9457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e74a2298aa2f2e09dcf9a682785087b9ca9e4d1c5d39f7b357be81865e06fe`  
		Last Modified: Fri, 22 Nov 2024 23:02:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a6caec45fbe24db114590c46f70bee1bfb7351bfb823ba705257af39da584a`  
		Last Modified: Fri, 22 Nov 2024 23:02:32 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64058e90a64e3e6f083f65ad2b49eb7db94907e5eabf60f389d23904f2b5d76`  
		Last Modified: Fri, 22 Nov 2024 23:02:33 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858df7fae105e7b7e788b34fc7f1ba1d19ce2f12836afb407e639cd8918e61d5`  
		Last Modified: Fri, 22 Nov 2024 23:02:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:186468c881287b88467d28ff1fc9cda8d844cb568a16a9e614f4680fca142b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.8 KB (633799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c213b433938ad49137e0de62b19141598abe94ff794a64bef0699ca7aaac8491`

```dockerfile
```

-	Layers:
	-	`sha256:3f4ffda465160b6a5fcdd8ce688aa4b754ad6530869abc72f615e174e2f94076`  
		Last Modified: Tue, 10 Dec 2024 07:35:05 GMT  
		Size: 588.5 KB (588463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8d33fd0f97089975b6433a7795ef991ed06d38fd510c172c703fb52cd5a7b1`  
		Last Modified: Tue, 10 Dec 2024 07:35:05 GMT  
		Size: 45.3 KB (45336 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.20` - linux; s390x

```console
$ docker pull postgres@sha256:56dcc9cd9c1f9519f96fc07072b86b479638e8cceab83b3a32adc67d0c9687da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104928586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0eea97c9e7bc41983f0492802fafaabefaca376c889dc6a9b15e0c8de8ae87a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Dec 2024 00:14:30 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
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
ENV PG_MAJOR=15
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=15.10
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=55abe738d441f0e58658b3ec6f88097a713b5e3b73139f6230d7b5c4c389e573
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eafe7c8b9860553fb2cea051416d72bda2987943eb8479b124d8a67a91ca6f2`  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a799b09b87fd567f09d6a428342633ea34aaaba594a1dbd1daacb8be0542db5`  
		Last Modified: Tue, 07 Jan 2025 17:38:33 GMT  
		Size: 1.1 MB (1079601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089de645761ac472ff3d3bbea2e6f5138887c6bd03bc46e26f7b477d0db60378`  
		Last Modified: Tue, 07 Jan 2025 17:50:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c40c652c2a358d06735f4751ca5ef4848a5a9b9792557d00856a9a0ff022ef2`  
		Last Modified: Tue, 07 Jan 2025 17:50:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b89d26ed50414eb9a222c231c8c4a26244ad2b9d26404412f76e1222cb4717`  
		Last Modified: Tue, 07 Jan 2025 17:55:22 GMT  
		Size: 100.4 MB (100373166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b157082d119581a4b275739bb845da6f41bba9216613db1749c1ec49b930151c`  
		Last Modified: Tue, 07 Jan 2025 17:55:20 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3675b3cdf18ab8fc7859fc6b12df4e129bdfe1e291ee7b49e1332b31e9846d`  
		Last Modified: Tue, 07 Jan 2025 17:55:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daf5391331ae1b68f6d952f6aeb2111996c50f8e9d95f8e0a88d8a5f4cbe7f2`  
		Last Modified: Tue, 07 Jan 2025 17:55:20 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea6d003d8eb4d3840bbd5b2dbb5e4c28d5fed5b3f5768476fa9f5bdb345c0cc`  
		Last Modified: Wed, 08 Jan 2025 05:56:19 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9140cb72e6ebc61941f7e06d47600941bd19fdf8067de3f331f558db42773e0f`  
		Last Modified: Tue, 07 Jan 2025 17:55:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.20` - unknown; unknown

```console
$ docker pull postgres@sha256:aaed465d00dfcdad48d3cc3bdf24e2f005b5fb99b308633e6414b6705a2c83db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.9 KB (632869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a3287bb9a9b9b6cf314a898738398467805233022dff341888677468eeeabd`

```dockerfile
```

-	Layers:
	-	`sha256:82fbf4ea9edac8abd006b788e1f6bfe0d0102f51351676de8a279f5633e4ec46`  
		Size: 587.6 KB (587575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e41478cdc6d61ad3fe745eb4627eabe56143a2e70e250e9188e8515506c1e37`  
		Last Modified: Tue, 07 Jan 2025 17:55:20 GMT  
		Size: 45.3 KB (45294 bytes)  
		MIME: application/vnd.in-toto+json
