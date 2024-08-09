## `postgres:12-alpine3.19`

```console
$ docker pull postgres@sha256:b566cfa2f577f3cf7d2eb779b3b9bdea368bec51ccde7025a17c1376fd4d341c
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

### `postgres:12-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:15eff8f66e0d120ec8603c9c462a45d4af587e2175b9d41722ab91126ba55710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93127291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5b55278578a806c4ea61d4103b4255517c857e63b919630dcdb40f5ff6cf06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_SHA256=2d543af3009fec7fd5af35f7a70c95085d3eef6b508e517aa9493e99b15e9ea9
# Thu, 08 Aug 2024 16:22:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b3b3848a907519d1db417746ced000af0165b22fbfe1d884aaeff69987c282`  
		Last Modified: Thu, 08 Aug 2024 19:05:17 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd3c6401799ec874e5b684b9fcb184261cc8ebdaa426816b029f007a55d9b3f`  
		Last Modified: Thu, 08 Aug 2024 19:05:17 GMT  
		Size: 1.1 MB (1120289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6421b65608f471b49f5ce4c31d7f858f44ae865fce1174b408d828bde38fa8a4`  
		Last Modified: Thu, 08 Aug 2024 19:05:16 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf11bba6fd41ade2c964084357fa66a9db44ada0eb145bc489307f00a0496fd`  
		Last Modified: Thu, 08 Aug 2024 19:01:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874bc6b3a310aeff560b8c5e47a9c2dc4bfce146b35526e372671be38707eece`  
		Last Modified: Thu, 08 Aug 2024 19:05:18 GMT  
		Size: 88.6 MB (88571815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24af348db0b8966ded8dbb13cce4d7c0cb0a46983abc37f3516056186ed3501c`  
		Last Modified: Thu, 08 Aug 2024 19:05:17 GMT  
		Size: 8.7 KB (8685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a7e4811a57380183ec20bbc6a95880c7f225da5d49e4ab19617173a3efb61a`  
		Last Modified: Thu, 08 Aug 2024 19:05:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9500f1b71a4041f1b39014012ea281b7a021a36e00b9bfd0643521c7cf8a9dea`  
		Last Modified: Thu, 08 Aug 2024 19:05:18 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac444c8ef670f0d8f78320066c846ff83d4fad0f4334b5fcc738ddcca2e10a2`  
		Last Modified: Thu, 08 Aug 2024 19:05:18 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642cab16df749ae50f9f8182bac21eccd008f95f585c34d4470108d82c75f372`  
		Last Modified: Thu, 08 Aug 2024 19:05:17 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:d361c2abef12dcdb3fd335d9f0efdc08ce1f2ab9aefbf7597c66ab154f884154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da79f1dbedc3a7303c433e08a0d41277384d4a93eff1bb83dee24d828db0d00`

```dockerfile
```

-	Layers:
	-	`sha256:3aa27339ee20099bfd1fc460819479a96458b632cf49546f3ef20be568c673fb`  
		Last Modified: Thu, 08 Aug 2024 19:05:17 GMT  
		Size: 965.7 KB (965737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe98c92ed9abed4ee555e1aa2bd63d6e89a0fb356075897ea8718c2e7ebec17`  
		Last Modified: Thu, 08 Aug 2024 19:05:17 GMT  
		Size: 44.5 KB (44507 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:1ba49dd781a5e7cbcf021e3e2072b7e135159ad9621f11c394076cf1ecb0781f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (91993321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a04dd2e474e5405aa03b4f4f36f6c7425c6bc3f634023238afe44a98d3e3c92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:22 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 22 Jul 2024 21:49:22 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_SHA256=2d543af3009fec7fd5af35f7a70c95085d3eef6b508e517aa9493e99b15e9ea9
# Thu, 08 Aug 2024 16:22:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92880c2baf59ed2b2161ddbd42912f3c667f88b880b2bf7c544e35241839cc4`  
		Last Modified: Thu, 08 Aug 2024 19:10:19 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61abd44f0f6a377f52eb7c5307b260122a9190bc60a8ebc1db65d929f490cb8`  
		Last Modified: Thu, 08 Aug 2024 19:10:20 GMT  
		Size: 1.1 MB (1086692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70361eae90d9585bb273a16d57620fe9982fb2233fae0aff2a0c20dc4102d53`  
		Last Modified: Thu, 08 Aug 2024 19:18:01 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfa82c1ccf85ec588942b557d525431c73d2d1c59629214d888e6d8341478f0`  
		Last Modified: Thu, 08 Aug 2024 19:18:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76a6f75f230665374abd9d408a9bcddc97c33feb0a4c05b7eb934b9d17af39d`  
		Last Modified: Thu, 08 Aug 2024 19:46:45 GMT  
		Size: 87.7 MB (87714813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e834a90607e0c32d42d5dc15d821b5b73a5961944181d66bbcef571f7abd93`  
		Last Modified: Thu, 08 Aug 2024 19:46:43 GMT  
		Size: 8.7 KB (8684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2c2bbfc26058bbeed29e7b1511870e3ab484346182deafe9c8f6c13641df9a`  
		Last Modified: Thu, 08 Aug 2024 19:46:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f1bcfc1d64e3bf17a78adeb57943bef17dff2a79cb652750e74ace91e535a5`  
		Last Modified: Thu, 08 Aug 2024 19:46:43 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c58ec7f44fc0fdf2bd65396eee643f606d202cbaa716a4a201478da492a3efb`  
		Last Modified: Thu, 08 Aug 2024 19:46:44 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b3779d93a751ce3b2d8de01dc74aa614b8daa2787cc9a03834cc3e7f96cd40`  
		Last Modified: Thu, 08 Aug 2024 19:46:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:e032b5972df42f8ec333a5d0a23042ee2701bdeda51af4afc2634971e89d02c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 KB (44446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef313285c0f8fbf4bd9832b5cd9c1dffb655515d6b81a27b5f32d7ade404a69`

```dockerfile
```

-	Layers:
	-	`sha256:c2265857eb727287fb6b3c2f6e7eaf19bf8d4731fd6a429b87da5d10d241b554`  
		Last Modified: Thu, 08 Aug 2024 19:46:43 GMT  
		Size: 44.4 KB (44446 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:373f5d5483fc6377fe1bb2cdcefcf5db8af505a0320a4b35d7340e2004df56ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86525127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81521d1a1626d6f9bed9d1accff6453716b04df899b7d3997dfda50d09c8a3a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:53 GMT
ADD file:60c2aa05ac383c09d9e77c7234444745ba6b4007cbe51e0c51d3c21b159b2b3c in / 
# Mon, 22 Jul 2024 21:59:53 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_SHA256=2d543af3009fec7fd5af35f7a70c95085d3eef6b508e517aa9493e99b15e9ea9
# Thu, 08 Aug 2024 16:22:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8f161eaa88b843263b696c64fddf3418b0e44eaf5043acda85e43596a2978f9b`  
		Last Modified: Mon, 22 Jul 2024 22:00:34 GMT  
		Size: 2.9 MB (2927105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063d9d2991cbf5efa23a343aaafc56190a3c3718bbaef42229b875284c56d644`  
		Last Modified: Thu, 08 Aug 2024 19:58:44 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d0a2dd7241794c1e2100b1dbd8912d9474e69be44f859e7cbd5419bcc2c208`  
		Last Modified: Thu, 08 Aug 2024 19:58:44 GMT  
		Size: 1.1 MB (1086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bba820d52c202cdcd219628b030bdeca3be564e0af977f5d726e9bc789f91d1`  
		Last Modified: Thu, 08 Aug 2024 20:36:18 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f9a032391fec40670850720f298f8d5e2cc62ee9dd48243f50d58d95a6b856`  
		Last Modified: Thu, 08 Aug 2024 20:36:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd7bb7363584efae21228cc8839b574650156648d00fa22e971fe568d5f55f4`  
		Last Modified: Thu, 08 Aug 2024 22:53:49 GMT  
		Size: 82.5 MB (82495185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c072b1af8664e1811c4492208571cf76dbdeca651a9a006855fd8f7bce0c1e5`  
		Last Modified: Thu, 08 Aug 2024 22:53:47 GMT  
		Size: 8.7 KB (8686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bcf405f6a1c3055742af26676bcfdf5e42f9ff89bc28a49b3fdfbe46c1a219`  
		Last Modified: Thu, 08 Aug 2024 22:53:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c4ef356bdfd6a7a801df75ecc7700136b47fb09cd1f6905f2d292f8d7f7e11`  
		Last Modified: Thu, 08 Aug 2024 22:53:47 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171f11a57c04d35656f156ca497be0a9bf4d251af9cf608fcaff7c85322634bf`  
		Last Modified: Thu, 08 Aug 2024 22:53:48 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56eedbdadd8aadf108fd40aa8f05925ce4f38cdaae9cdccd8810168c2be32db`  
		Last Modified: Thu, 08 Aug 2024 22:53:48 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:a90cbddbc199008d20bd51d7f91ab116fb254aa802d69fe8d525a52f1da60223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2de55989276848b0ebe92af95d2f4dd01e4356b4b61d4bbe1689b9dc9c89304`

```dockerfile
```

-	Layers:
	-	`sha256:c2406382f1422e6af14fdbfc4c115e213293db253a181d1eacac179005fc883e`  
		Last Modified: Thu, 08 Aug 2024 22:53:47 GMT  
		Size: 965.8 KB (965757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5684680a610465c10deb7b0a3ca1a8736594b939110a054d0e3d5cc0cb9a3bdb`  
		Last Modified: Thu, 08 Aug 2024 22:53:46 GMT  
		Size: 44.7 KB (44665 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:2b6755a691a2660eddd92d25bf9d31b9cee805c81e5120391442b9823911d025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91899269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9687a7a234f3e91b8dffe12eac5d660e6b4cbe3537d0273ecc62f6a0cdc19ebb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_SHA256=2d543af3009fec7fd5af35f7a70c95085d3eef6b508e517aa9493e99b15e9ea9
# Thu, 08 Aug 2024 16:22:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3c3a45049e949f25991f4ed3e907fcbf34307ac290a2e4b00b184d7dc461b0`  
		Last Modified: Thu, 08 Aug 2024 19:19:00 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a48cf11d206c8fb70c1d16f7316613ce43ca94cd0a15ce1e7fc054358defd5c`  
		Last Modified: Thu, 08 Aug 2024 19:19:00 GMT  
		Size: 1.0 MB (1049348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d8f6666a6359dc964d8bc9b9b8ce6d373b710789596fa942fc294e0b8d2449`  
		Last Modified: Thu, 08 Aug 2024 19:26:47 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254a903eb5ab79247f4b63556539e18b675b25772fe95ab54cfd0f62eddacb02`  
		Last Modified: Thu, 08 Aug 2024 19:26:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ec5b46f296a4e25f51be31a5b94aac0802d93d287a4e56c3a60f7869bd8752`  
		Last Modified: Thu, 08 Aug 2024 20:06:31 GMT  
		Size: 87.5 MB (87475314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32242203677b7b063ab60bd7e02f9f763d1ca712f82bbec425b2fff96b7c09dd`  
		Last Modified: Thu, 08 Aug 2024 20:06:28 GMT  
		Size: 8.7 KB (8688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edc5f594cc14925348b6ddd12c753552663f4d8eee69eb79f02cf1b52b3e9ec`  
		Last Modified: Thu, 08 Aug 2024 20:06:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2abc4145f6b481f06843e2f17d5614c03e854f4a1dd603f3361ec18750515c`  
		Last Modified: Thu, 08 Aug 2024 20:06:29 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bdbfe700041a8e56b6634f029eb42f507b4c091d119a4b8d5bce663cb2bdfd9`  
		Last Modified: Thu, 08 Aug 2024 20:06:29 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00162dab6b8fe4dc4bd67a56a71d8c6fa42260cb10b6a7212c387f4c26bb7769`  
		Last Modified: Thu, 08 Aug 2024 20:06:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:2cac74d0a7a828926acd4a5867a7edd5441a44d0b5324e4c65a70b5a871bc394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8125cd8fd6568a94eb5c4c7d042178a280421986b804fb85aa63960b1d44df7`

```dockerfile
```

-	Layers:
	-	`sha256:a3d7157a68b27592264cf2116b5a7555518c731fdeb1455a941f80742f18a78c`  
		Last Modified: Thu, 08 Aug 2024 20:06:29 GMT  
		Size: 965.8 KB (965769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1817c4e2dccb1c1f5cb920f7433c369b7ec7c2cd662ac03fe382af6f9cfc664`  
		Last Modified: Thu, 08 Aug 2024 20:06:28 GMT  
		Size: 44.8 KB (44783 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:013a70b98cba4fe84b821d07de20041fe03442641d482946676c71e97caadb0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98319550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bcc74b20a06fa14e18648bd75edcf636adeb080ec477f83daa7ec9dd6bc16e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:33 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Mon, 22 Jul 2024 21:38:34 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_SHA256=2d543af3009fec7fd5af35f7a70c95085d3eef6b508e517aa9493e99b15e9ea9
# Thu, 08 Aug 2024 16:22:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa1b630a0b5d0bb81b65102beffce632e6e7caeaa492a50e752fa9460e3431b`  
		Last Modified: Thu, 08 Aug 2024 19:05:57 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95eea2d3d235283c641316aa8fa94393d7bf34bd97068a9fd1aed8460b963bd9`  
		Last Modified: Thu, 08 Aug 2024 19:05:58 GMT  
		Size: 1.1 MB (1095472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be58be95aa866ea29ab3b7513edc8a0dc6d7b8f661a3ce28fc6cf1e3d718b68c`  
		Last Modified: Thu, 08 Aug 2024 19:05:57 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a72446e5e24f6040e2844eda3f7062f68116e5e0cd1901fb8a6fa79edfbbca`  
		Last Modified: Thu, 08 Aug 2024 19:05:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe58e91f61f61c6d1b046d8ff19e6e95fac349584187bb89e979f64e7fc4cbcc`  
		Last Modified: Thu, 08 Aug 2024 19:06:01 GMT  
		Size: 94.0 MB (93955333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531bab4e71720ee629102ccef8ea07a616b8b4c09e43819d9c49e34a9d6de6a4`  
		Last Modified: Thu, 08 Aug 2024 19:05:58 GMT  
		Size: 8.7 KB (8684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fd24a14203939070e3c10eaf48ce5db1916e5d8f3f16502d870a98cbdff710`  
		Last Modified: Thu, 08 Aug 2024 19:05:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486cebf83e120991a1fce5c2d19fc77879be134978378965fe10730830b62030`  
		Last Modified: Thu, 08 Aug 2024 19:05:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33d34d45ac47fd6301dcd9c8eaf40bf114668ee60173c6dc5340dee32143772`  
		Last Modified: Thu, 08 Aug 2024 19:05:59 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaf5aa665f56acdd8e54bb94fcc159a282b94574109ec8538e0ad1c4b1098bd`  
		Last Modified: Thu, 08 Aug 2024 19:05:59 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:aca6c4926cd613b361119ae5b43e1bcd6d92ce3c0c829b0ac142f44123b91fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1010193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da85b4cd1ab274fb7207a1355fe0367e98e3a2ec586c3dfa7e4c4e1003e57e1`

```dockerfile
```

-	Layers:
	-	`sha256:5d3a2b5a20481ad4987f9b6bc9309e07b7ccdd3201822c35c37ac8283008c0a5`  
		Last Modified: Thu, 08 Aug 2024 19:05:58 GMT  
		Size: 965.7 KB (965722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85004beae1037f8b8fb9ddf72e60973e4720896c7e5fb72ed9b721a0ba23fc7e`  
		Last Modified: Thu, 08 Aug 2024 19:05:57 GMT  
		Size: 44.5 KB (44471 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:cdae114cf33ca32b1177b8b44df6c5c7f1cb96250b5a4ee94ab46fb6e293de15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97506864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40867e43f90bdee4265176de7c64b73a6605ae4650765f7fe5685e26ce7cc26d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:28 GMT
ADD file:0a05f9aa9e288df7339330e9c8c7654e92a33000bb227984a095f716196f51cc in / 
# Mon, 22 Jul 2024 21:26:28 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_SHA256=2d543af3009fec7fd5af35f7a70c95085d3eef6b508e517aa9493e99b15e9ea9
# Thu, 08 Aug 2024 16:22:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6822b2fabea056adaf2dbe133c4384939c5aa1e2a522e965ebda31e26deca1e5`  
		Last Modified: Mon, 22 Jul 2024 21:27:04 GMT  
		Size: 3.4 MB (3363106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43c54eaa4f98734ca302a76f3612cc2053a98ce8eae19a9c437a93d2ac61ebe`  
		Last Modified: Thu, 08 Aug 2024 19:31:07 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d174deb4fd213ac5cb7a3716aead941aee3fe54810cb126b17054b131ff624d3`  
		Last Modified: Thu, 08 Aug 2024 19:31:08 GMT  
		Size: 1.0 MB (1039694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca1921cc69949d708b558fdb3a1c56217e55aa445257c7e77d85bc383f7a5d0`  
		Last Modified: Thu, 08 Aug 2024 19:40:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1e9fb2d97e779240090a94d2fb1530246df6ec0372eab82cc473a1a687791f`  
		Last Modified: Thu, 08 Aug 2024 19:40:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ddf7a042bcbe4456951acc699932e4a029eb5cb2c3c16041f891a1e25d8f4d`  
		Last Modified: Thu, 08 Aug 2024 20:19:15 GMT  
		Size: 93.1 MB (93087914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c3f4e5b63eca9770d2e24873aa48d80adde53d6da474968430c00d9c891b4a`  
		Last Modified: Thu, 08 Aug 2024 20:19:12 GMT  
		Size: 8.7 KB (8686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f84f255c0a7ab5cf57c46adb735891cd34fbe01bfecd40c03dffbcc36c978a`  
		Last Modified: Thu, 08 Aug 2024 20:19:12 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4c6feea224d6d11e8825f2b5584301e1faf1617827f3fad57853fac4bb4344`  
		Last Modified: Thu, 08 Aug 2024 20:19:12 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa024ce33e9805bc181f1dd17fd0c7e5eeae720714077cbe3252a045c136deb8`  
		Last Modified: Thu, 08 Aug 2024 20:19:13 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6214cff0e6d520750b4c58ee5d1c6ddf5a2dec1672f700e6e7ad8347da1b8c21`  
		Last Modified: Thu, 08 Aug 2024 20:19:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:5dec78d4ede79500ebefc69069c917921de43d9c3d536490a4f72ad7854addc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1006690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73412546f1b456afb27f40a38cff2faa3b34c169cd8de6137714ed9dc02b8186`

```dockerfile
```

-	Layers:
	-	`sha256:ce52e521207fbb1c013974c9361388b2ab8c5f9530d4a44800d3cca45a24c98d`  
		Last Modified: Thu, 08 Aug 2024 20:19:12 GMT  
		Size: 962.1 KB (962141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8bfa8fa3476ae6d859af5f248ca0da237f9410191209df8de609d272d75b350`  
		Last Modified: Thu, 08 Aug 2024 20:19:12 GMT  
		Size: 44.5 KB (44549 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:e1c8c6b657718a75224e2ea7cf37d9cb40b490cb3bfc0e5ee55e135a589f3ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101824635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d05f52243e9057d04ca267de0e1d926e4977fe0c7439851507eedf4cb08b0c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:18 GMT
ADD file:b52033eb72014ee086783e139c55b353697322576013415769016a48fd4f4342 in / 
# Mon, 22 Jul 2024 21:50:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; ln -svf gosu /usr/local/bin/su-exec; su-exec nobody true # backwards compatibility (removed in PostgreSQL 17+) # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_SHA256=2d543af3009fec7fd5af35f7a70c95085d3eef6b508e517aa9493e99b15e9ea9
# Thu, 08 Aug 2024 16:22:52 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1f544ad804b60fa6fc54acddfe2c176a2b22e7079fedbf238b2c2bb51b8d0dfa`  
		Last Modified: Mon, 22 Jul 2024 21:51:15 GMT  
		Size: 3.3 MB (3253076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5319fb43b1caf84617607cfcceb185eeec884fc0061f7cf5b8b64cca1bbe09`  
		Last Modified: Thu, 08 Aug 2024 19:29:47 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6816ffa2083c875ab2e27a897be7542a64257e7b9ae0768523a494e65f9fbe9f`  
		Last Modified: Thu, 08 Aug 2024 19:29:47 GMT  
		Size: 1.1 MB (1083896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589ff1270482aa8a8fac0fe3f79a08124f053efb32c3b366c36f45b1d31a1e5b`  
		Last Modified: Thu, 08 Aug 2024 19:55:00 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba2ae1f10a13eb92260472341c10e536a57b5c22f6a5de6f8fc6415f049654e`  
		Last Modified: Thu, 08 Aug 2024 19:55:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d2c2db282b2e4ef5fac0e4b26da8a65987e678baf63ce78f07fcfae30245a0`  
		Last Modified: Thu, 08 Aug 2024 20:51:12 GMT  
		Size: 97.5 MB (97471518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59173ba88c92be319aa79813750177242bbc61eb0d98f2345bd9dc52e3191ab7`  
		Last Modified: Thu, 08 Aug 2024 20:51:10 GMT  
		Size: 8.7 KB (8686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20551ec9da26abf9a30218495abc5e0ce9e2074b1d2e7514f482efc68c424ef`  
		Last Modified: Thu, 08 Aug 2024 20:51:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de2044e2d16d02a0cdb281d0eb8348f1d3ac7ef5e50586b9449d7a3bcb81715`  
		Last Modified: Thu, 08 Aug 2024 20:51:10 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f392a74aa86826e0f35ab22c08089ac895140db93c16855865b4a95d96e2fb5`  
		Last Modified: Thu, 08 Aug 2024 20:51:11 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0061bd21b01a9f35d27ef58ec025dc44d217a23c4d559f5ea8e8156dea799438`  
		Last Modified: Thu, 08 Aug 2024 20:51:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:025f88537155b0c932e24b0d272bd30afbe61e0a142e29716e32c0c0b7469f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1008290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe054a3c47c7ef7696ef6fe703909bcc4ecde577bce27b669b914fe04748ba5`

```dockerfile
```

-	Layers:
	-	`sha256:33a0455582b1b5a5ad8684bd28fae4d58fd4b1c11184a44b514a3d8018847e1b`  
		Last Modified: Thu, 08 Aug 2024 20:51:10 GMT  
		Size: 963.8 KB (963783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f96ca1728af8b3389f9e46cc98fc6e31ef55fd8ba4f70bd37153e2146c800ec`  
		Last Modified: Thu, 08 Aug 2024 20:51:10 GMT  
		Size: 44.5 KB (44507 bytes)  
		MIME: application/vnd.in-toto+json
