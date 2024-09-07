## `postgres:17rc1-alpine`

```console
$ docker pull postgres@sha256:7014ff9d256cbc4b9894f7092754b98ad8064c85e1a09cc91206cbf28104de7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:17rc1-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:064adfeaf4127666dee6f6386a6c1bef41952927894c1a668daa6f6600a7c051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98745175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d16168495824c42e35f234a27de008fe29b8682bac68abe2d53daeec2b7cb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17rc1
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_SHA256=cef689e2de8c3d605d8406c065573b8d70859fc6f2a8d720b0d98a6d62ef16e8
# Thu, 05 Sep 2024 13:44:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25307227c90bae58c84dab41277d5472d9cd00151c62baab3eec8f0811c54942`  
		Last Modified: Thu, 08 Aug 2024 19:06:01 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6ad02c3e211165e47b37a87649b86bd72f65170d27f581321a4650a888cdf9`  
		Last Modified: Thu, 08 Aug 2024 19:06:02 GMT  
		Size: 1.1 MB (1086466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04587a03ca55d1cdcc36c6341a8ebf7ba19e4066cf3c9e59914a6ac4350c68af`  
		Last Modified: Thu, 08 Aug 2024 19:06:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77042b8c8b0cfbb3da4fb82e75010d4b98354b5cced618b9dfb1450fb9b7a7a5`  
		Last Modified: Fri, 06 Sep 2024 21:16:21 GMT  
		Size: 94.3 MB (94276642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd61b7f2882661308d5abc79d8ebbfa33807f6791635a613cad9bb108e5fdda4`  
		Last Modified: Fri, 06 Sep 2024 21:16:18 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e47f52ad6b545280718ae73f05d1cffba6bebb5fcbb3f2bc56c023e93bf563`  
		Last Modified: Fri, 06 Sep 2024 21:16:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609d8e14591b1ee547e24c3088c5f8585446a598d7f363abe8961b4983ccf08e`  
		Last Modified: Fri, 06 Sep 2024 21:16:18 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fc600d6ca3a6ee21891e84946e2f05fd3fc6d4103d0cb7a76d7dbfcdfef3d7`  
		Last Modified: Fri, 06 Sep 2024 21:16:19 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad34d14bf64a8a5081078d409637ee5bb678e5cab147f51885adbb91867b82c2`  
		Last Modified: Fri, 06 Sep 2024 21:16:19 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:8eea7ec31dcf7c602487692806876afa857d3659f261319850273c6bda0e804b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 KB (42313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99536bb26b300e7a4f2c244550c3a4a603ec686921469b964b4a1f7c59664204`

```dockerfile
```

-	Layers:
	-	`sha256:7e96e71db37a17c7bbe1a429334de65b12f2a22df209fb6eecead250b4157ee1`  
		Last Modified: Fri, 06 Sep 2024 21:16:18 GMT  
		Size: 42.3 KB (42313 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:00bba0589f131f0810be593bfdfb4f247aad3e222a3c0b55f48b3b1eea29d61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (92958948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477493362be332c34eb3604ad627f05f9c3422a92e3f24231e4e077d044ea6f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17rc1
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_SHA256=cef689e2de8c3d605d8406c065573b8d70859fc6f2a8d720b0d98a6d62ef16e8
# Thu, 05 Sep 2024 13:44:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06c96dcb42dd8bdc51a58c85dfcaa19dbfa92fe29d1a4a654a07d90235128e3`  
		Last Modified: Fri, 06 Sep 2024 21:37:20 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5481238d23101ac993d20caf4639505438d7f64148b13ec11c12a9893158b2a5`  
		Last Modified: Fri, 06 Sep 2024 21:37:20 GMT  
		Size: 1.1 MB (1086471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264614f0c6349218facc6d4a5b53ea0e454c7db2acefae78a30d876c6c5e1794`  
		Last Modified: Fri, 06 Sep 2024 21:37:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820b815a00ead51bcaf5fee800ea6d818cdee4a48b1a40d0ef186d06628aa6d6`  
		Last Modified: Fri, 06 Sep 2024 21:37:23 GMT  
		Size: 88.8 MB (88760632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1cb08bc159c423441ebca229debdee9b4ac7b4c41475aa6488e54ef76f2ce1`  
		Last Modified: Fri, 06 Sep 2024 21:37:21 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4660410352fd3d3912360c8e5e3226a558b814adb0ab9db31b0739e035debdd5`  
		Last Modified: Fri, 06 Sep 2024 21:37:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59aa9c7a20778b3fd8498b0a1dd5b114d80d98956fcdac71a4eccca526e732e`  
		Last Modified: Fri, 06 Sep 2024 21:37:21 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9386e608c67b9bda05ca20199465985e9c40bcdf41161224880e19a5bb7276`  
		Last Modified: Fri, 06 Sep 2024 21:37:22 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3035207e2cab31f198470f8057fae6d3ac4637ac085c55d3f746c491a74b0a3`  
		Last Modified: Fri, 06 Sep 2024 21:37:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:92a9f9709c65fc6b288808bc24cec2a5a19ad256b24623e40efe114cfbdf36b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.6 KB (632633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f307745bfa20030ac50ba0e46dd1eddee24b9926d72e7d0fc89de558752df3dc`

```dockerfile
```

-	Layers:
	-	`sha256:81024f0c77171510eb13528c57a219f6a291d693d666484715c517c6f9f109cf`  
		Last Modified: Fri, 06 Sep 2024 21:37:20 GMT  
		Size: 590.1 KB (590099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:281973b3153ecf1456cc84f62612c9338a75831f9d01f6c7e2aad8917a8d17c0`  
		Last Modified: Fri, 06 Sep 2024 21:37:20 GMT  
		Size: 42.5 KB (42534 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-alpine` - linux; 386

```console
$ docker pull postgres@sha256:f1dc84fbf5c24868f5f9edd5406fd81f5d9835443a6e6fb56a3b9e707bbe4e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105578397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9081f4a670c82f76dd234be1f2a8e4f67df6df15f519c77e8515030fa83440d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:29 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Mon, 22 Jul 2024 21:38:30 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17rc1
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_SHA256=cef689e2de8c3d605d8406c065573b8d70859fc6f2a8d720b0d98a6d62ef16e8
# Thu, 05 Sep 2024 13:44:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadf224e4e0f7b5031e505091dd4014d757e5215b53e3c68375ec69e2ea8149e`  
		Last Modified: Fri, 06 Sep 2024 21:04:53 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf7fbb7545b113e541c3824438dff476fe646ef486e925ddd55ebab19b01e23`  
		Last Modified: Fri, 06 Sep 2024 21:04:53 GMT  
		Size: 1.1 MB (1094853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eff05a9bf0233b9bf097c07463de77189f8f69f904750b31d46979a44017cad`  
		Last Modified: Fri, 06 Sep 2024 21:04:28 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a0250847e0baa37c46b4bfb3fa2c2c4c79c739edcc843486ba51c1fd165300`  
		Last Modified: Fri, 06 Sep 2024 21:04:56 GMT  
		Size: 101.0 MB (100998602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d4e6f89c95f0821801dd8d74c8a2c87ae5137d03023b377ac908bfde18a438`  
		Last Modified: Fri, 06 Sep 2024 21:04:54 GMT  
		Size: 9.9 KB (9879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d67df46982fbf655abcae5d83fbf74bc8feccf0e6a2df4bb7a59262b348303c`  
		Last Modified: Fri, 06 Sep 2024 21:04:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6a93849a42e0ba31128602b087006e1c61e7e2410dfa887ff5b422981b776b`  
		Last Modified: Fri, 06 Sep 2024 21:04:54 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95f0732da8036cfd582c545a913b4ba009144691802bd3a8d05a97bb16abcb8`  
		Last Modified: Fri, 06 Sep 2024 21:04:54 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468221b01f16108edb5d0f7959899f5b258a22e4968eadc7a58e4c2a23d2a128`  
		Last Modified: Fri, 06 Sep 2024 21:04:55 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:1f474d57a068cbb5f70e9ca77bf9d9d4dce8a4c1b04598b0bbacd8e02b04f22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.4 KB (632424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc98833b80a04916d36943e3dbf19355e4eb04d3f2fef1af5f0e610b7f8e44a1`

```dockerfile
```

-	Layers:
	-	`sha256:0ebacf243c7fd08148ead8cd533f58d373c7f6b2babdb0529abd52ee9aae072b`  
		Last Modified: Fri, 06 Sep 2024 21:04:53 GMT  
		Size: 590.1 KB (590064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53260a9eea30d1317d5bab3ef63fa16491920eac5ceb9ab18fa1d45acf9707ce`  
		Last Modified: Fri, 06 Sep 2024 21:04:53 GMT  
		Size: 42.4 KB (42360 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:ae7198e25b3f166a3198adf37289930ed56c9dad002e6f63e1ecce4e3387cb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104899467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af50e554bbbda637f74991c7becff650656ec98bc32b711987589a14afe5f47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17rc1
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_SHA256=cef689e2de8c3d605d8406c065573b8d70859fc6f2a8d720b0d98a6d62ef16e8
# Thu, 05 Sep 2024 13:44:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5605707ba5d1754c2657fd2de6d69810b4b582f84e8942c4aadecb28eae47d`  
		Last Modified: Fri, 06 Sep 2024 21:03:37 GMT  
		Size: 982.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32ccc17fc1483dd4090662e5b4cac6178ea295c4e80b5ce7e03c376f6b7d344`  
		Last Modified: Fri, 06 Sep 2024 21:03:38 GMT  
		Size: 1.0 MB (1037919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c82827a1f99f74c579cc3b97868aacbc925cc3d91df0a1465624d1d286ba6db`  
		Last Modified: Fri, 06 Sep 2024 21:03:38 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ac4a07cdcc79bcbb169be9a8a12e424816f0509cd2088c50d80e0accdd5364`  
		Last Modified: Fri, 06 Sep 2024 21:03:41 GMT  
		Size: 100.3 MB (100273115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fccda59764226ec9288c50a3197a150fd7b27637ca8b32c066e23f92ae6351`  
		Last Modified: Fri, 06 Sep 2024 21:03:39 GMT  
		Size: 9.9 KB (9886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853e2f984bfe394c80050d2f244060f2b60b105b09ca676d160a90a86b26790e`  
		Last Modified: Fri, 06 Sep 2024 21:03:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0418b78c6896ff73cce040b90da16b0396dd69beb025147a65491fca9a5813af`  
		Last Modified: Fri, 06 Sep 2024 21:03:39 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4607c6961bc1bd9cdb0eb40c8c6918b6a4d39b8ab82f57ab136e799f9fdd0f83`  
		Last Modified: Fri, 06 Sep 2024 21:03:40 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd6390e3b4deee8a648966fef75c822d5ba6f7e359a1d57a1dfa10bab7c9ee8`  
		Last Modified: Fri, 06 Sep 2024 21:03:40 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:b3bd824bfa84a0e8a63b50e4f8a223d7637eb05545996530391409a4630109f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.9 KB (628918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50eee0c8cd9410cb260b79a370c22a3c4e9d1b4e43466568e83d6f59f596104b`

```dockerfile
```

-	Layers:
	-	`sha256:9d547912ea084f95e0b46e6952e8cc17fc82501252dc3cfa27e01fcef07bc58e`  
		Last Modified: Fri, 06 Sep 2024 21:03:38 GMT  
		Size: 586.5 KB (586483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55193d113ad382aaae30a6fd2979f7be5a07dfb6150f2871f6426a293db68916`  
		Last Modified: Fri, 06 Sep 2024 21:03:38 GMT  
		Size: 42.4 KB (42435 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:16974593ed04c0e7037a425c60ed5d17bdd339d300ec49db539811d2eae5853e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100214266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ae95327ffc8861148792391ae1ce2af988f2e8500d5834c952196c5573af45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17rc1
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_SHA256=cef689e2de8c3d605d8406c065573b8d70859fc6f2a8d720b0d98a6d62ef16e8
# Thu, 05 Sep 2024 13:44:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb1c65214fcacb9f32e742abec8b92bf683b2e7a7be27073b203cf9dc5d4574`  
		Last Modified: Thu, 08 Aug 2024 19:58:50 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a4e93ef12922da34742cb49015c46af1058cc89f480318d1346da5ee6f8f47`  
		Last Modified: Thu, 08 Aug 2024 19:58:50 GMT  
		Size: 1.1 MB (1087952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7238cbed1aae3da443bfe309847860758a3c4a8780cd5b0292ea5bf444f45c`  
		Last Modified: Thu, 08 Aug 2024 19:58:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e616c85d7c993a0ccb11cab3c8392086aa2c33e3567e4879c22b2222b74c17`  
		Last Modified: Fri, 06 Sep 2024 21:51:12 GMT  
		Size: 95.7 MB (95738739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466c8daa13aedb468d8d0646fa2f990b43948ab14d1cda80df32321e06647134`  
		Last Modified: Fri, 06 Sep 2024 21:50:59 GMT  
		Size: 9.9 KB (9893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e74c0ac3468c04388701f3b1468dcfb27b0a9242beee9d074ab27940c982a84`  
		Last Modified: Fri, 06 Sep 2024 21:50:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7821bb300b0c5cae592a5737a504416a52ce2b12a19f1d9d3ff2eba93d1882ac`  
		Last Modified: Fri, 06 Sep 2024 21:50:59 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffafbee5bff612d679a3bc4f528e2cd32fba365ddd1070f863a30d259b7d16e`  
		Last Modified: Fri, 06 Sep 2024 21:51:00 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679a37ff5b694eb1e11aa537f6e4898a44c685cb05d1c83d280514e48f800a92`  
		Last Modified: Fri, 06 Sep 2024 21:51:00 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:221f12a05c5229bad283036ac90679a636aa526eeb30b16031d3045b8b776183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.6 KB (630572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10318da4a261e6ac98e15624f7930418f0826315feee5c88c5d0806da273f49a`

```dockerfile
```

-	Layers:
	-	`sha256:aa916a7b4ead33aa96f9cc85e83a80047dcfd8bbe22153c5074482c6466cce8e`  
		Last Modified: Fri, 06 Sep 2024 21:50:59 GMT  
		Size: 588.1 KB (588143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60a29502dedf15fe59b06a5baf34c3aaa8b6e97098ceb7d6a32cb030078cc7c5`  
		Last Modified: Fri, 06 Sep 2024 21:50:59 GMT  
		Size: 42.4 KB (42429 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:a488c7b958bd29827835d543e93bd0e236dbbca56c8997028643a3e77c164e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109069483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca09827007f26bdcc513e2c8c92981bcad616d56b9bffe9116b7e6c4d942841`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17rc1
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_SHA256=cef689e2de8c3d605d8406c065573b8d70859fc6f2a8d720b0d98a6d62ef16e8
# Thu, 05 Sep 2024 13:44:37 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce2bfa3c4731d14e8b99a59a584f17c1226a95a67b0466b416abfc3c74076d7`  
		Last Modified: Fri, 06 Sep 2024 21:03:33 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cf41db10fff5fcdca8ee005a82aebccf5f7ae01fbd9a8cb7dffab9aa3af67a`  
		Last Modified: Fri, 06 Sep 2024 21:03:33 GMT  
		Size: 1.1 MB (1083301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be2a4a8dd21bbef55a42deafa9118da8aebd824555a60013c04badf572b53d0`  
		Last Modified: Fri, 06 Sep 2024 21:03:33 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26034db65460ae055fa775aadb2e556d1f39571eba35acef56772a4649f9e6da`  
		Last Modified: Fri, 06 Sep 2024 21:03:35 GMT  
		Size: 104.5 MB (104508236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80a6529f6e1e264b1d4464863287444207fe09c6fb8287e86be27cb669c8d60`  
		Last Modified: Fri, 06 Sep 2024 21:03:34 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa7d3657c341c09e14937763454913a95d30695daed0440dc354dab4449b83f`  
		Last Modified: Fri, 06 Sep 2024 21:03:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc08e3d28fb5bd45fbb661002b6aed2b684eed6c7b518021bd7ffbbc898e1aa`  
		Last Modified: Fri, 06 Sep 2024 21:03:34 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d42c48fc118b946ee9d2a182c94db8e1a1bc0a744727f5666699de4fc0d8223`  
		Last Modified: Fri, 06 Sep 2024 21:03:35 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966710039d8470cefff4e087be018307bbffe6927c74f7a8cbdeeddc6ebb661d`  
		Last Modified: Fri, 06 Sep 2024 21:03:35 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:5db04d6cc0421b4704abc09937b03372ca1d6bccdf1d620bb489e0fb79b8bf76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.5 KB (630520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab086023488e3f4fb1ef7e140e9efc67e3dbe73c77624c1ffff81c713981d0e7`

```dockerfile
```

-	Layers:
	-	`sha256:b1508e9fddf5ca7cd67b7c0a7d16afc048f6c9a4953eb6069444e0a092bbd872`  
		Last Modified: Fri, 06 Sep 2024 21:03:33 GMT  
		Size: 588.1 KB (588125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:909c2e5d6ce40484602fdf09c30c84f54e51ac2f0a3bd42c0fb91e787348ace0`  
		Last Modified: Fri, 06 Sep 2024 21:03:33 GMT  
		Size: 42.4 KB (42395 bytes)  
		MIME: application/vnd.in-toto+json
