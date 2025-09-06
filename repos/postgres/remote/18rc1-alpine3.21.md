## `postgres:18rc1-alpine3.21`

```console
$ docker pull postgres@sha256:4d9ae801041c2dde0d9ca08279b4b3f970b2e498a2081862a4e7b0174c35ec0f
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

### `postgres:18rc1-alpine3.21` - linux; amd64

```console
$ docker pull postgres@sha256:c12d448f23c6cb6d23f73c4878121f40e1aa9fd1d32b576bc16c28661382531b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111655109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7c48e21b38a371f22c25ef9b977f6a88f870d1ecdd037ab48b7fd33efe914d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18rc1
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_SHA256=b1a4cdc0ed6e97d117f044da67815829d560002c821290a9dee86e5e499b2f4c
# Fri, 05 Sep 2025 00:02:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425bcb58cfb84fd895ddfed1870ff77b64678179d86746c79b90ca12112cc7a0`  
		Last Modified: Fri, 05 Sep 2025 21:51:18 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7befeeae373f9dd2e581d335908d3d93800c752d7c5f0f818b06874f199bc03`  
		Last Modified: Fri, 05 Sep 2025 21:51:18 GMT  
		Size: 1.1 MB (1115524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51348e5dbdab63fe893b2a42718503294ee2c1a3bd82995186c0a495f186036`  
		Last Modified: Fri, 05 Sep 2025 21:51:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ebf62d24d035893eaf3fa3c2584c534e86bbfc5ae5627b717a6d39de5db4c9`  
		Last Modified: Fri, 05 Sep 2025 21:51:26 GMT  
		Size: 106.9 MB (106875725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356029a27d7cbc76f3360476d49ce72f13b17853e0a534deb64680b8886c456a`  
		Last Modified: Fri, 05 Sep 2025 21:51:18 GMT  
		Size: 18.8 KB (18775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04340b142758fae22c20e817039789251aecca6ffb27663eb8b17ff8f3213fbc`  
		Last Modified: Fri, 05 Sep 2025 21:51:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18a1d6fee199e8ba201007d724442d6dc32c03dca70250b84b66c0115a1c383`  
		Last Modified: Fri, 05 Sep 2025 21:51:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de15c19065be1f62ae5e3561ce831e37bfdb01e83e2cff249e33016495913e0c`  
		Last Modified: Fri, 05 Sep 2025 21:51:18 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83774c0ce9ecaf802b4ba1825e216dee2319b6491d4966edab0db73d257935f`  
		Last Modified: Fri, 05 Sep 2025 21:51:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:d454c4e8f801b2dc2bfd3ee75580ccd542e6256f083d11eb91ce1a1c72ea4fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.4 KB (639421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f24a09c9b1145a83913bff7aa903a58a6b0ed5feec45f9e727a0461c9bb8901`

```dockerfile
```

-	Layers:
	-	`sha256:42558b8899c820130248dfe7b3108fcb9f3a522f4a96509d3bb7427fe35cece2`  
		Last Modified: Fri, 05 Sep 2025 23:13:58 GMT  
		Size: 598.4 KB (598380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03755088b937aee24d51d34883a5758ccf183f1ede19f42cc6e13ae0ed3721d5`  
		Last Modified: Fri, 05 Sep 2025 23:13:59 GMT  
		Size: 41.0 KB (41041 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-alpine3.21` - linux; arm variant v6

```console
$ docker pull postgres@sha256:00fbc6f46ba87bcaae5e6636d03f6ce820127607366d8be8d6e37553da82e325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91254270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b45a10823c3566aa0614553697a1dd7b36c8be7ca08ca718f5cb4c334e3a711`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18rc1
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_SHA256=b1a4cdc0ed6e97d117f044da67815829d560002c821290a9dee86e5e499b2f4c
# Fri, 05 Sep 2025 00:02:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e574e747df0785c7236aedf2522008d435adce4848514534a408f92e9c80447d`  
		Last Modified: Fri, 05 Sep 2025 21:50:46 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2e5271c8d19b847d492447bccca6a0c22d8c36fc9d2702ce6b58bf57815033`  
		Last Modified: Fri, 05 Sep 2025 21:50:44 GMT  
		Size: 1.1 MB (1083480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f9bf8a2c105397419d425ff188bc1a3c6725e3d57dc48cd0e58705038ba022`  
		Last Modified: Fri, 05 Sep 2025 21:50:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f160d9a75fda693c6eb6223304decaf7ae885b6079cdc0bc8b0c0c66c750801`  
		Last Modified: Fri, 05 Sep 2025 21:50:51 GMT  
		Size: 86.8 MB (86780686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcd82e1345847bf6508192d8bf3a91bd1d59aa63d716dc21d1e36318af7f936`  
		Last Modified: Fri, 05 Sep 2025 21:50:44 GMT  
		Size: 18.8 KB (18777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884dc99cf52ff42bd5e7d2dd188f4d66155e719b46ab1cfcb7d0cabc4b541ce0`  
		Last Modified: Fri, 05 Sep 2025 21:50:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4124e1f1bd6bb83141f07b814eeb2269f6824042648c637f4da2f49df707eb49`  
		Last Modified: Fri, 05 Sep 2025 21:50:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c64e797c4e5ffe1eb3de29dd2478bee8dad89363f27a8d3436221f3f3f3898`  
		Last Modified: Fri, 05 Sep 2025 21:50:44 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fde75cc0fb99813deb211338c4065f1e89f70730a6f8e4d867653c63d025491`  
		Last Modified: Fri, 05 Sep 2025 21:50:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:d1bfe826201775367e9b7126622c801c5cd449408532102431a92fb5753b13ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 KB (40967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bf23a7901f9d29d2ca5fbcfce6bdd0957f7c64c975952e908cb3a5aba1dfd8`

```dockerfile
```

-	Layers:
	-	`sha256:b5290e38a3d813e63c6798e6f710444d22972ff69ad43bd33e6ad6133ca95ce4`  
		Last Modified: Fri, 05 Sep 2025 23:14:03 GMT  
		Size: 41.0 KB (40967 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-alpine3.21` - linux; arm variant v7

```console
$ docker pull postgres@sha256:e81163c174d4db70cab1395df8aab7b4f4bad22ef15ec8997b545d1e2248877c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86401085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3798a6f21244f98c4120f42ff62f3368e50039f76da82c09322a1071e4b506e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18rc1
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_SHA256=b1a4cdc0ed6e97d117f044da67815829d560002c821290a9dee86e5e499b2f4c
# Fri, 05 Sep 2025 00:02:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48741ed7f0072c8c20c520f3ee390a44573bc2c76a47a8dea14be96594b7522`  
		Last Modified: Fri, 05 Sep 2025 22:08:22 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e52656bbbb57298021ccbfa82b3418534d3aaa1cbd51e533de531f57771983`  
		Last Modified: Fri, 05 Sep 2025 22:08:23 GMT  
		Size: 1.1 MB (1083497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06a43acf3b00ea063599d29f103f735aa47f8081300c9cd41a51b1778c9cc84`  
		Last Modified: Fri, 05 Sep 2025 22:08:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58507073c18deda2655d3c7161d47ed0a20fb6355b2fadd8084f3c84c38fbb76`  
		Last Modified: Fri, 05 Sep 2025 22:08:32 GMT  
		Size: 82.2 MB (82194439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7002eb915df9a90f351655b67dc4251b2c4789b88aeda4029617c2a52c60176b`  
		Last Modified: Fri, 05 Sep 2025 22:08:23 GMT  
		Size: 18.8 KB (18776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b6ed810e169fa274ea9b671d18d9b9293278fee8fc6aaf4a73460036cf0da6`  
		Last Modified: Fri, 05 Sep 2025 22:08:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73642bfc25b2759ad0e629bf4c8d75ee68621979460a81c5b9b1c2cfff0bdcf5`  
		Last Modified: Fri, 05 Sep 2025 22:08:24 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4046c3c9f214af62d8020bffc63d2e17099390181364fa1f01e60f232ddb22c5`  
		Last Modified: Fri, 05 Sep 2025 22:08:24 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5197ccda64ffb36cf6c1617038b39118ef3679c8885b0493b51b73273282c1b8`  
		Last Modified: Fri, 05 Sep 2025 22:08:25 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:9f67188a56b1fda1585865bd95a73f9f86470e38f08692e2dcb237b385dce034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.6 KB (639574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5435d238a67b3bac6e9dccbce2cbbce289daf52dc65acf03e6d7274ce2f8197`

```dockerfile
```

-	Layers:
	-	`sha256:30ffe95f822a89c5341a7acf6e7327cfa3b805f634298a6855f23fa6bcbf83ad`  
		Last Modified: Fri, 05 Sep 2025 23:14:06 GMT  
		Size: 598.4 KB (598392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759a6b81a5274d5cda541fec5f5a3e94f1b873ee15682fb261dde0fe967ef50f`  
		Last Modified: Fri, 05 Sep 2025 23:14:07 GMT  
		Size: 41.2 KB (41182 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:de9ecb4d89895e8df4a972697e50e356b114be685869276f64dfeef0eaf5e256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107537286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc35674aa4edd418890cd58eef7697b04eb5adf836595773d1148261f690598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18rc1
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_SHA256=b1a4cdc0ed6e97d117f044da67815829d560002c821290a9dee86e5e499b2f4c
# Fri, 05 Sep 2025 00:02:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d99875a637d0146395097033f5d685eef44e33b155235238b8fdd16d95788fe`  
		Last Modified: Fri, 05 Sep 2025 22:10:13 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6afddfea3dcc1b95bfdcc7050bd638e524cfed5fcd89b43e66eaa9bebc29e79`  
		Last Modified: Fri, 05 Sep 2025 22:10:13 GMT  
		Size: 1.0 MB (1042480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749696547c8485795e383c0aa07766bdee59c1549985500317d797ba1f94d266`  
		Last Modified: Fri, 05 Sep 2025 22:10:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b068aa9ffc36268234fb3f1c262d89bea9f84be25661fe2198f8a02be2c28ee`  
		Last Modified: Fri, 05 Sep 2025 22:10:19 GMT  
		Size: 102.5 MB (102481581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f2a6f25ac9d63f15bb5743ebfbaac7bba871f14f5ac869fc59e55838d16b76`  
		Last Modified: Fri, 05 Sep 2025 22:10:13 GMT  
		Size: 18.8 KB (18775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f37b30a36c01742310acfe10665bfdfe83a962ddedb2458902b32c77da5583`  
		Last Modified: Fri, 05 Sep 2025 22:10:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8bce33911d57228acb3b603adcc9f58d203f2cbe8f9992b4bd9aef62839de4`  
		Last Modified: Fri, 05 Sep 2025 22:10:13 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52098656453e10e7fb45ce77f1a19c913eb70694774bb5b42070f7a0bf775b1`  
		Last Modified: Fri, 05 Sep 2025 22:10:14 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afc7902d82b8326e1a60707eac414617da6a06c64977c75757778348b3ab8b8`  
		Last Modified: Fri, 05 Sep 2025 22:10:13 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:a8d38a309cf22405589af70fd540a09f91e19f2941e0a2804d6cc3a540f53dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.6 KB (639614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7408ed4efada35b6ec91ef903a82cff8d14d81722de0f267950e0cb4953489`

```dockerfile
```

-	Layers:
	-	`sha256:120776b0aaadefb489240aa3af6297a5d5cd2a58f2ab08e6c7de9cf153b77c25`  
		Last Modified: Fri, 05 Sep 2025 23:14:11 GMT  
		Size: 598.4 KB (598400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:500ab71a918bcb87cd4af50e895ea21e28be69239afc496c94279b0bc743bd94`  
		Last Modified: Fri, 05 Sep 2025 23:14:11 GMT  
		Size: 41.2 KB (41214 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-alpine3.21` - linux; 386

```console
$ docker pull postgres@sha256:17a0ad016024b2e43015ccdfe191336b0a52dadaefb748ba05ffad3f41029957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117913340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2752e451519d733a12fb785afacf0fd28a96fbf2cd4e798f604fa48be5e497a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18rc1
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_SHA256=b1a4cdc0ed6e97d117f044da67815829d560002c821290a9dee86e5e499b2f4c
# Fri, 05 Sep 2025 00:02:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2994f6168e4d2f89215852ae98fd3182f24c622758e37739f5b18e7dd0f11711`  
		Last Modified: Fri, 05 Sep 2025 21:51:53 GMT  
		Size: 973.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980e11c3c9e77d095e319795333b0f9df6f95d80c509a5cde7100865b1982772`  
		Last Modified: Fri, 05 Sep 2025 21:51:53 GMT  
		Size: 1.1 MB (1091458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643657dc7982253369d93ee12fcf87234882814b9eda071d5ca9f8c89809e3f3`  
		Last Modified: Fri, 05 Sep 2025 21:51:53 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eefc038903c2016928eada8c446f17cfe583bd6717836849e67a1cd3e08bfd7`  
		Last Modified: Fri, 05 Sep 2025 21:52:02 GMT  
		Size: 113.3 MB (113334873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6907a5ebe20c20c6e3fd9593178df4a599f44920e54d3bc9ff2d60867a5afb`  
		Last Modified: Fri, 05 Sep 2025 21:51:54 GMT  
		Size: 18.8 KB (18775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2526b27c99a8cc69246d2c2506ee3cbadd037cb86573034f38ee60d454753c41`  
		Last Modified: Fri, 05 Sep 2025 21:51:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18d2456dda76715f3808036342588b21a882008001f95a243e3bd8504e24abc`  
		Last Modified: Fri, 05 Sep 2025 21:51:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9bc4d41831697635f9eac91bc27b7d5851ed5c78d1de67b343699153f2e0e7`  
		Last Modified: Fri, 05 Sep 2025 21:51:54 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db61cbe9b7f69705890c763b49f4f572cfa46935b39a957b115e633d8d3e8e0`  
		Last Modified: Fri, 05 Sep 2025 21:51:54 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:4479026729878cf4266afd615f1060c86b823358252edad26ad0fd9352461f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.4 KB (639380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f649da7cdfb2f495ea43f9f7eb633d94324bf1927ecfe5c6b2630f3ab883ad32`

```dockerfile
```

-	Layers:
	-	`sha256:4739fcacfab38f34ead47273e312708c79ad6bfdf5aca625eb869c89ecb4ed09`  
		Last Modified: Fri, 05 Sep 2025 23:14:15 GMT  
		Size: 598.4 KB (598370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e14ade2867e2c34a7e733241fe8eee140f9f8e0bfec07a9fda361a0c8b397fb`  
		Last Modified: Fri, 05 Sep 2025 23:14:16 GMT  
		Size: 41.0 KB (41010 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-alpine3.21` - linux; ppc64le

```console
$ docker pull postgres@sha256:a0059210a886a8f65fb21c8fc56459971e0deffc0055c6755f623ee3bb50ec3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95551780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280c2e71dbb1a76123a654de806c6e41cc937d3684d5da0612c64a2d159a2cc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18rc1
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_SHA256=b1a4cdc0ed6e97d117f044da67815829d560002c821290a9dee86e5e499b2f4c
# Fri, 05 Sep 2025 00:02:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1852ad0fcecf42ec3510333344e4d74df585437a9660291e490ff0eb089eb0b`  
		Last Modified: Fri, 05 Sep 2025 22:25:50 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab03a4f7ee38dc2683e073deab226686b6ced595ed156ccea2c340ff47c7e58`  
		Last Modified: Fri, 05 Sep 2025 22:25:50 GMT  
		Size: 1.0 MB (1032147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cddd2e04a87a62ef84c413d11aad215ce268f146df007d7b99815e18d54889`  
		Last Modified: Fri, 05 Sep 2025 22:25:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4538959c6179d1ba8252fafa2794a1a02b33a46738d55e93b76afe2f84a18c2d`  
		Last Modified: Fri, 05 Sep 2025 22:25:59 GMT  
		Size: 90.9 MB (90924208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8b61005dec4cf7f81d720579b38fe444f71b2268e17ac35eb268794d96aa79`  
		Last Modified: Fri, 05 Sep 2025 22:25:51 GMT  
		Size: 18.8 KB (18785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a8c92216ae4203b43e1f03a79415be8daae4184916e662557abf1a8e1aa5a0`  
		Last Modified: Fri, 05 Sep 2025 22:25:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb1bc5b9eea789baf07ea9fc38e729f309e2b6d0ceed4394d3fdf64568bafc8`  
		Last Modified: Fri, 05 Sep 2025 22:25:53 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd05e42cbe496b836d231545cb465d32edbb8867b30ab67bd2550e20512d82f5`  
		Last Modified: Fri, 05 Sep 2025 22:25:53 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a394ad116be209c0af49e8418c99fc54e931dc4d9b04828cc100018e0d9e37e`  
		Last Modified: Fri, 05 Sep 2025 22:25:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:9597416bab5d980ebb5c6dbb50952300bfc82021349fa5b85823b7b601358285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.9 KB (635858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e9424b4650633713de2114b2472f217f1d023c8b77f6983c88c3b1d91741b8`

```dockerfile
```

-	Layers:
	-	`sha256:5ef9abbfe7572de13690b1ed1a98165ea0a44b9716914b4eaf41ca396b1b31f0`  
		Last Modified: Fri, 05 Sep 2025 23:14:19 GMT  
		Size: 594.8 KB (594783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05cb74e8e76898f99e7409b5bad0ab925576d1c70d56d876d652836a0e99f157`  
		Last Modified: Fri, 05 Sep 2025 23:14:21 GMT  
		Size: 41.1 KB (41075 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-alpine3.21` - linux; s390x

```console
$ docker pull postgres@sha256:f932f1744f7859d5e76e45aada5306b352a4bd87e04e58668da871e374beef82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120313909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffa79078ead9b8f59abd02e5f982465d7284e08a44c7ac12d062f47c7941698`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18rc1
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_SHA256=b1a4cdc0ed6e97d117f044da67815829d560002c821290a9dee86e5e499b2f4c
# Fri, 05 Sep 2025 00:02:55 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1eda89a85cb2447477faa16e64af3c86c61e779fe35232248cb1ea8af7001b`  
		Last Modified: Fri, 05 Sep 2025 22:44:27 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630202f1d29a174bda8ea87bf83b65e950395d2fd3db14560e5a2c0f6fde23fd`  
		Last Modified: Fri, 05 Sep 2025 22:44:28 GMT  
		Size: 1.1 MB (1081098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8a4422ad505a3d18535391db603a1d5d6f87673e91deda1361f7f5c416abfc`  
		Last Modified: Fri, 05 Sep 2025 22:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91a422c934c1ef2743197494dd72eb31c70c41b7e022e8261ef66d1d074693d`  
		Last Modified: Fri, 05 Sep 2025 22:44:33 GMT  
		Size: 115.7 MB (115744416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a19539930e1caf3197fd3777aa7b84f74cabe85f076b2519d34a8a719c4c35d`  
		Last Modified: Fri, 05 Sep 2025 22:44:27 GMT  
		Size: 18.8 KB (18780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadd9cce174c478fb950a33729bed59781faa5f3bda91261686f7cad73bf99b9`  
		Last Modified: Fri, 05 Sep 2025 22:44:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d670202dd3ff3a47aa3416a89edf95f1e8f77c28d542b1d3bb445c1962968fd`  
		Last Modified: Fri, 05 Sep 2025 22:44:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb25257a5cb8606094d66a9e06741e35af73e810d13776ef2b14d6b655241c1`  
		Last Modified: Fri, 05 Sep 2025 22:44:27 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7da8ccf58fe92e8306cff25770f4edf0ad5deb50758457c46060d0b7646f05`  
		Last Modified: Fri, 05 Sep 2025 22:44:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:126042120eddf00681e906a0e5392e7dd12b765e4e901b56317392624b094bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.5 KB (637469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0228acce783e2846db32486c132535009a4b31619e47431116b9c1763b85c9a`

```dockerfile
```

-	Layers:
	-	`sha256:702bab0979f324a69941cee009e519caee19530af506f8213280eda6d2c85cd8`  
		Last Modified: Fri, 05 Sep 2025 23:14:24 GMT  
		Size: 596.4 KB (596429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0849ea0e75d61a858a32b21e966db25586b0fa9607221c68aa91c75e8c280df0`  
		Last Modified: Fri, 05 Sep 2025 23:14:25 GMT  
		Size: 41.0 KB (41040 bytes)  
		MIME: application/vnd.in-toto+json
