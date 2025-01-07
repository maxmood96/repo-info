## `postgres:17-alpine3.21`

```console
$ docker pull postgres@sha256:d37d2c160d34430877c802e5adc22824a2ad453499db9bab1a2ceb2be6c1a46f
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

### `postgres:17-alpine3.21` - linux; amd64

```console
$ docker pull postgres@sha256:80666029fb5be9fb4642a9e59f2e1362d2c6c968c09325a03125cf1887a46890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110574467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc0916eb67945fd8b6d8cab1acdd18096294dd827d87b2cd0626f7f43bce5c70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=17
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=17.2
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=82ef27c0af3751695d7f64e2d963583005fbb6a0c3df63d0e4b42211d7021164
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75a4b03c1eebcc4c02bbd97cb57fec7d46a8e87c63ed2de869273d5f1d4e769`  
		Last Modified: Mon, 09 Dec 2024 20:41:45 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b21501bed01f4429d8b07a9b12c246decec998c133165bb0569f66f9078e6fc`  
		Last Modified: Mon, 09 Dec 2024 20:41:45 GMT  
		Size: 1.1 MB (1120802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c0e2b7ab303ea9286cd2d511ca3e89ea653a85fadff40b089d1e75cc31170a`  
		Last Modified: Mon, 09 Dec 2024 20:41:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a5ebc6841c2c8c18b7d4d2030a7fa0f5896ef0157e071d46be64f2ebe00e7b`  
		Last Modified: Mon, 09 Dec 2024 20:41:47 GMT  
		Size: 105.8 MB (105792342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4c933cd88b948e48e7a8cb39ed68a00721d19cd434aa3f6793377393372f27`  
		Last Modified: Mon, 09 Dec 2024 20:41:46 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7123cd9f3565a24e338650c2556f748bc1e546891372385150983a92d60e001`  
		Last Modified: Mon, 09 Dec 2024 20:41:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe216961f214bb8f5e59c5b5edbf47487a373f9e3dbd94821d1f1c33e5395c58`  
		Last Modified: Mon, 09 Dec 2024 20:41:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99f4f35ab9f6a0afa60cc3bcd46c0859b3b11b75de0f1665fe0863eeed74c21`  
		Last Modified: Mon, 09 Dec 2024 20:41:46 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66a800d2b4f7c83acf9df47499693cb23efb4c6a2c74811545a86450da162b2`  
		Last Modified: Mon, 09 Dec 2024 20:41:46 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:00903892391d555da1a41208dc6788f8c43eb8d7b5337507066b92f4288e3e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.3 KB (640340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c343f61fbc661c5c4b3694f2c6f3e8da16d224022cec9d3cbc2b13a13343c168`

```dockerfile
```

-	Layers:
	-	`sha256:06d5f8046b3f8830b716bbb42c6f8bf99a9f38808be8b21f95d1ef5f0fb43df1`  
		Last Modified: Mon, 09 Dec 2024 20:41:45 GMT  
		Size: 596.5 KB (596526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ac9f23ad01021edabc7738d98e872ea11727c40ac4e0fd925a40a2d878b6716`  
		Last Modified: Mon, 09 Dec 2024 20:41:45 GMT  
		Size: 43.8 KB (43814 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; arm variant v6

```console
$ docker pull postgres@sha256:098a2b2bd1207a845f869266e76b6aef6c68c6c158492664a3c0970dc3c3f402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90141818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a39abb8e031987085b06d67a5bdbf3967c3054315a5adb9529ef64456712ac9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=17
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=17.2
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=82ef27c0af3751695d7f64e2d963583005fbb6a0c3df63d0e4b42211d7021164
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb193193ddc35962e0dafdae114651b8d4ba1e59fcf576b26e6d97250d1b3e9`  
		Last Modified: Tue, 10 Dec 2024 00:56:17 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece0f3da96be66bc605327add1a1323c98f39d0f953ebac1e199fd55c8b781b4`  
		Last Modified: Tue, 10 Dec 2024 00:56:17 GMT  
		Size: 1.1 MB (1087886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655d9097608d513ade2437ac121d1e82392c919bbf163e99a9ea6161464bcd8b`  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c0f10f66b38c6d3b6050cbf8c9a7045ce805a36c1c1d2cd3e7d4dca1621b95`  
		Last Modified: Tue, 10 Dec 2024 00:56:20 GMT  
		Size: 85.7 MB (85669865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2417d3db5cf80fd876b822b86868c8ef2a251540c8451eb5ca2b038845de0141`  
		Last Modified: Tue, 10 Dec 2024 00:56:18 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decccd5fdd1e67c86b559b812265e42f0e5233fd676aeb52c28ec3de8fbd28a0`  
		Last Modified: Tue, 10 Dec 2024 00:56:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777a5304654dddf49852e7e7297571383fe2c56d37344eebfb1ea76517968f9f`  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d02786d12aed1eb1608b4a7d70dda2b06d305ca6b365c18dbc462a0b1c551c3`  
		Last Modified: Tue, 10 Dec 2024 00:56:19 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87ecb86b3f2b69b54ed7abfcca256b18ad7dd7cc3aa3dbd2b24abdb6f459f3e`  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:df756af7fdd5b72872cae85f1b86132247778e2e01b5a393e5afb61b88616a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 KB (43776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d53195fc3f34e06ce9f318746ddcbebfe2df617c7f42be141b3b265f60697c`

```dockerfile
```

-	Layers:
	-	`sha256:13e5fac065057bf719c8f74dc8bfdea4767339b8971df50a264ef5b8520fd8b3`  
		Last Modified: Tue, 10 Dec 2024 00:56:17 GMT  
		Size: 43.8 KB (43776 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; arm variant v7

```console
$ docker pull postgres@sha256:8b308e80b3578558423c0d3cd64506bc75bde647f5ed876a0f6e61fb70d12b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.3 MB (85338547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ec111483f3f817347ed6216be2550497d4c7287936fd979e4b1752c1724792`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=17
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=17.2
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=82ef27c0af3751695d7f64e2d963583005fbb6a0c3df63d0e4b42211d7021164
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a83ffa7fea6d8e44df866bf0431b4aa7353bc126de7c0655ca2138c5ae5662`  
		Last Modified: Tue, 10 Dec 2024 02:38:24 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3ef3c8f59874acb6e75d5c3e946a3d5bc6098a33bb9462103d4e1b933619fd`  
		Last Modified: Tue, 10 Dec 2024 02:38:25 GMT  
		Size: 1.1 MB (1087888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d925f8dae9282aa521d5e72cbfaafc927fb428264cfd4f30ad68ab41fa49216b`  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2d902daff98ded12eccffa6a3b8f2bdeb95006ddd65ee583cb9e9951ba71fc`  
		Size: 81.1 MB (81133735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a83c71b74204d23f28bc621dae0270dc4515d26b010a224a86531d4e09766e`  
		Last Modified: Tue, 10 Dec 2024 02:38:25 GMT  
		Size: 9.9 KB (9886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2f487f945fedf7a6d3a1dd03e75805df62f2fc7130ae8b1e06a1b644320e80`  
		Last Modified: Tue, 10 Dec 2024 02:38:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d96de489ef26b798c125a5ed1faf3e0ddc00fc8274d0f48efaeb8ec37f8574c`  
		Last Modified: Tue, 10 Dec 2024 02:38:26 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5810282ec8ecd7092a173f6a11e6659ed28fa395f4aa6134c3fafa79db57e0b5`  
		Last Modified: Tue, 10 Dec 2024 02:38:26 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050fce2741d6b8f38839c1f154065d71c58a38bda649bc23b0403a8ac40975f1`  
		Last Modified: Tue, 10 Dec 2024 02:38:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:c67df4b00b1499918b0945dfd7069196da86630a7c013fb7ab49c117a72cadeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.6 KB (640570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2902a559d3fee2dd7738cba571216d1a3d807df00f37fbe3fe8753e141186fb`

```dockerfile
```

-	Layers:
	-	`sha256:1f9dea851844346259e5efb510077aa1cbb73a46fef6e8a61c8c2671bf0809e5`  
		Last Modified: Tue, 10 Dec 2024 02:38:25 GMT  
		Size: 596.6 KB (596578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d468de27744bdeb2fff4609d1c6c8579331b63f0e6666ec85eb28f1d4db0f6e`  
		Size: 44.0 KB (43992 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:38f86f4eccf6e08bcf32325f9caabd25d24bbc4e92ddd6baa83dbb0365174618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106456273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311abe301881452ccbc1178478dac5c1a7511898f46c533cfd4bf1c57db7a49e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=17
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=17.2
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=82ef27c0af3751695d7f64e2d963583005fbb6a0c3df63d0e4b42211d7021164
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba0f6608f6f3d27568dfc4c9519be8aa4c533a0ba0a1e71e0776577186a0e26`  
		Last Modified: Tue, 10 Dec 2024 00:03:34 GMT  
		Size: 982.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63177b68728387376c02debb563d2af6b33d46e131a5d49837c4aa4df42a093a`  
		Last Modified: Tue, 10 Dec 2024 00:03:35 GMT  
		Size: 1.1 MB (1052573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f22355032538026f66f2457a5fab332d96c7316b79e773e8644007a4e7459d`  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1541d00733fff02ca359a8b2b82909d62888e25ce16d08297408210723e3fc8c`  
		Last Modified: Tue, 10 Dec 2024 00:03:37 GMT  
		Size: 101.4 MB (101393625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21efde2356aa5b976ac8f8e6da206dddf502d8577f80d792580196be0d525634`  
		Last Modified: Tue, 10 Dec 2024 00:03:35 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd95363b5e02123b344acd29ecb6c84349db7e9ec6ac277192166927d4d94559`  
		Last Modified: Tue, 10 Dec 2024 00:03:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b302ee014f4d7d0499844adb6bad2efe4d76de0474d63baf44e1dcc805dcd7`  
		Last Modified: Tue, 10 Dec 2024 00:03:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd34c6591ce92987c82672e2c1f10cda0cfa643b93f0405d51efe88c0f92d45d`  
		Last Modified: Tue, 10 Dec 2024 00:03:36 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9745fdb6743ae42ab31a8f9e4b526e552cea6824187d72e83153a5cbba6fdc`  
		Last Modified: Tue, 10 Dec 2024 00:03:36 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:40a09d466a35c74292dcbad135133998e0f05a90b2cb420c22c49432e407f47d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.7 KB (640654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b81c79c6c776254a2f20e8cf2052cbf9c34d1f756c16d302c603fbd194d53a4`

```dockerfile
```

-	Layers:
	-	`sha256:e4f67e5366e266582d892ec7033c978c518f6ffff9b4eeead19c7ed42357b8eb`  
		Last Modified: Tue, 10 Dec 2024 00:03:35 GMT  
		Size: 596.6 KB (596606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa3d2abca69f833e33006d1f52b6d64bdd36566bc70111e7c3d39ea1ffe17833`  
		Last Modified: Tue, 10 Dec 2024 00:03:34 GMT  
		Size: 44.0 KB (44048 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; 386

```console
$ docker pull postgres@sha256:2925996447b96e279814daa4fd53e034350ab9630b11edf0b5263b6f3b7dc612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116751145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f38451b98bdb824fca9ece9f18e0198bc9f7b3e0795eb08dcbe2b27db695f0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=17
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=17.2
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=82ef27c0af3751695d7f64e2d963583005fbb6a0c3df63d0e4b42211d7021164
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a263f935ef7113346a925e5191e410904b71a484f4c8bf1d565ca226ba3dd25c`  
		Last Modified: Mon, 09 Dec 2024 20:44:46 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2673c27d07bc1b7464963c7aa1cfa64cbdb792ee881fbc7f17128743a47c5a4c`  
		Size: 1.1 MB (1095938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f2def98f378674c3d658c835a56f24dc2845d62d46f7d784a2902762104f1d`  
		Last Modified: Mon, 09 Dec 2024 20:44:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12dfc967e7d172ec5d1209a0c6c9d21acf2265fa6400d255d2dbbacc7088505d`  
		Last Modified: Mon, 09 Dec 2024 20:44:49 GMT  
		Size: 112.2 MB (112172244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bef06e59f8d20e94ba269946131f67f32c2e0067910715d9020cea85400492`  
		Last Modified: Mon, 09 Dec 2024 20:44:47 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5141dacd9750a7a95d57fb5e3413af640fa58d30b6dbe7b46eadc2a3bff08`  
		Last Modified: Mon, 09 Dec 2024 20:44:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ac785e3bc9252d151ad6763805f21623e6c033574d61f1ade06b63dd9b4476`  
		Last Modified: Mon, 09 Dec 2024 20:44:47 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ed5d00622cea4790d07d151887f3da763199198319473f1ae63d33d95ff2f1`  
		Last Modified: Mon, 09 Dec 2024 20:44:47 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3160d5b43735af1cc08b3a542d7c83026f411697d88f0dbbcb067616421eb87d`  
		Last Modified: Mon, 09 Dec 2024 20:44:47 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:ed45b739b262c1a3befd7909b6b88d86d8c98a08012ff267507197a854ac7b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.2 KB (640250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82190c97c3a351802776e6b6c795e0ee57381f3c99cdf0fcfd44248c34ba4b61`

```dockerfile
```

-	Layers:
	-	`sha256:e92432aa0df4f9324f7408a155ebb0959b8f064af9c7067956534dec9a7c8430`  
		Last Modified: Mon, 09 Dec 2024 20:44:46 GMT  
		Size: 596.5 KB (596491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54bc6596093f5a6fa22b137cdb828341bbe17dccd8d79140e539024bf2e4fe09`  
		Last Modified: Mon, 09 Dec 2024 20:44:46 GMT  
		Size: 43.8 KB (43759 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; ppc64le

```console
$ docker pull postgres@sha256:7579b80956ac9d0b06f953f5ad400cc790ed59bd7b7bec552aa4f48e367844eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94354929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30588c8cf0c439957b3cffd5cf890f593569516f2c949ba4bc598d01c1f7cfff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=17
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=17.2
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=82ef27c0af3751695d7f64e2d963583005fbb6a0c3df63d0e4b42211d7021164
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4211206b6d877de6171a0dfdd86f904b33ba6ab31f8c4e945f6f1e1234b5b1f1`  
		Last Modified: Mon, 09 Dec 2024 22:24:47 GMT  
		Size: 983.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b682a4f7842bbe4fe5702944759dda58e8efd44117a67855aea727dfc1fa7e`  
		Last Modified: Mon, 09 Dec 2024 22:24:48 GMT  
		Size: 1.0 MB (1042260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2e3e1cf0ca8d87f9ac5be8b86e6b9d39903fba705596ae32b167667ec69c7e`  
		Last Modified: Mon, 09 Dec 2024 22:24:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c11f44a5d25528044b2f9b695825c0c4a19a1c4836136d83fd62621f411ae2`  
		Last Modified: Mon, 09 Dec 2024 22:24:50 GMT  
		Size: 89.7 MB (89718671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9febc7094fb139f9c1ac40942acccca7ee2f479dc9ff6a6a9087b379b534f471`  
		Last Modified: Mon, 09 Dec 2024 22:24:48 GMT  
		Size: 9.9 KB (9889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e337ec4732cfa9bd5cb9d56dc98798435b9bb2ac63b39610d92259d3b1f410e`  
		Last Modified: Mon, 09 Dec 2024 22:24:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9061b73c9d7a4905345c2c4c34040f8561fea9cf534957100f9c032b8f0524d`  
		Last Modified: Mon, 09 Dec 2024 22:24:49 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c837730e2e33610c10b8bb55b32fe703222483cdbc47e7fdd7ba64de77bf9cd`  
		Last Modified: Mon, 09 Dec 2024 22:24:49 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e798c8b7adae4a5c0906056e3cccfca73d1f57489aac913ee868235201b35c`  
		Last Modified: Mon, 09 Dec 2024 22:24:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:06935930a49daa99542837a6ce067d3a517b2d7b27b499859764766a53f82dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.8 KB (636833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a3cd5cb67f86891b50e52f70983a9a8b99ced45797d0c91c0dceafd175f636`

```dockerfile
```

-	Layers:
	-	`sha256:08bf16628e70e83877e1b3acd73e000e8842a71357ea5a7f8349170a232262c4`  
		Last Modified: Mon, 09 Dec 2024 22:24:48 GMT  
		Size: 593.0 KB (592954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5afc11a076d9de48e4b3c7056003a5bdd5cc83df00f394d43a224224f75b878a`  
		Last Modified: Mon, 09 Dec 2024 22:24:47 GMT  
		Size: 43.9 KB (43879 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; riscv64

```console
$ docker pull postgres@sha256:c9af32f51add54dad03ea3203fbb4016fe96103fd7a73c966b85fa8464d707f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110683150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919fa6e7fab26a08ace287a8cb158d5056ffdabffeae46ad831b3f07eab9ab83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=17
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=17.2
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=82ef27c0af3751695d7f64e2d963583005fbb6a0c3df63d0e4b42211d7021164
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1dea23fd35b1b2137e20c9f0c7d93cd055d0e7684137991907363db0d39c8b`  
		Last Modified: Tue, 10 Dec 2024 05:44:51 GMT  
		Size: 989.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f737b43c2933d58c075f6d291e04f55dcac95cb1aea8e77dc599e92d07ba38`  
		Last Modified: Tue, 10 Dec 2024 05:44:51 GMT  
		Size: 1.1 MB (1091676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e648c51faf78f51680225a4976f5bb41300ade0877e94087ac036d4a828786`  
		Last Modified: Tue, 10 Dec 2024 05:44:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5913c95dfc834a73da0e19367feb4478415744e48c22660619306ed23e3ee6`  
		Last Modified: Tue, 10 Dec 2024 05:45:06 GMT  
		Size: 106.2 MB (106220550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66b21488c1af1d68bdc0855281c0be56de31aecce2cb88fc37a8fe3c1662f03`  
		Last Modified: Tue, 10 Dec 2024 05:44:52 GMT  
		Size: 9.9 KB (9892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a4e2ea8c3dd6260817303601222fe2cae7f66c53da8e470b519177fc81d201`  
		Last Modified: Tue, 10 Dec 2024 05:44:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2d73df551000e13c94740ba10a2b07158e81aaa22f47c4fd504912078b0d35`  
		Last Modified: Tue, 10 Dec 2024 05:44:52 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bb19b2550a1e07044051ba307a7322b30503aa4131c7be15774239fd57586b`  
		Last Modified: Tue, 10 Dec 2024 05:44:53 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a4d32c009858497178819f1327c62e701bd4d4c22053b5751238b780d953ed`  
		Last Modified: Tue, 10 Dec 2024 05:44:53 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:d0ca323b8adfde2e25ea9521d810636d63c73185cb7851d18ace524d8cdf8525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.5 KB (638499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6300488c02a0e3bd397b1b164f04077bae525f6c3c14eaff34b03bc1e9b2c4e`

```dockerfile
```

-	Layers:
	-	`sha256:07ff719bc4333435e431b9fa1451c833061b893c6e5fa7a8dc3fb47ffa76913b`  
		Last Modified: Tue, 10 Dec 2024 05:44:51 GMT  
		Size: 594.6 KB (594614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04013cfaf68fc63262073cc9466c10c412dd69c0b719df74e92beabe48381dc5`  
		Last Modified: Tue, 10 Dec 2024 05:44:51 GMT  
		Size: 43.9 KB (43885 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-alpine3.21` - linux; s390x

```console
$ docker pull postgres@sha256:4e1ec7576d3bc9d9bb303eb0874b0671d7f9ebbcdd5685638e87cb783d4b5ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119136637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b96cadc2dcaff686eb08b8a60c338ca6519157f9aec5c490d6d2c2771dd157e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV LANG=en_US.utf8
# Fri, 06 Dec 2024 00:14:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_MAJOR=17
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_VERSION=17.2
# Fri, 06 Dec 2024 00:14:30 GMT
ENV PG_SHA256=82ef27c0af3751695d7f64e2d963583005fbb6a0c3df63d0e4b42211d7021164
# Fri, 06 Dec 2024 00:14:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm19-dev 		clang19
# Fri, 06 Dec 2024 00:14:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm19/bin/llvm-config"; 	export CLANG=clang-19; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0021c9a649801fdec18b4dfa0cef7e898cbac45e8af7c1a061898ca089adf221`  
		Last Modified: Tue, 10 Dec 2024 02:00:56 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51091c93fe9d5918bd5b2c172b26d7ad17a5c2b5009f331bacd2032be8b9ddc2`  
		Last Modified: Tue, 10 Dec 2024 02:00:56 GMT  
		Size: 1.1 MB (1086507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d169d1eddaa1dd45c130ac80ca43455d6918877b8bcd4dcee87a69006b3840`  
		Last Modified: Tue, 10 Dec 2024 02:00:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c52eba9e0786b697ab582c4cfdbc362d725b808cc870f3da07c206e7a49afd`  
		Last Modified: Tue, 10 Dec 2024 02:00:58 GMT  
		Size: 114.6 MB (114563720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad5a4105e8f22b2cc3ca147a4a5af64862676fed8d2e205de8175f6042f34cb`  
		Last Modified: Tue, 10 Dec 2024 02:00:57 GMT  
		Size: 9.9 KB (9886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43978be87ad8ff59599809aa80f9d0c1177712f7c4233977fd031b28f3514790`  
		Last Modified: Tue, 10 Dec 2024 02:00:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9815bf68e5e3204828a735d613d5b2a7080985789e15ba36eb6d07027bfda7d3`  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3615cc30bbd7c99d2e02c0e2c92a169bef6da62cd587dc0e7480c701745f61`  
		Last Modified: Tue, 10 Dec 2024 02:00:58 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cc9fc314fae9c8778cb3dc06077db6ba0960b7563cf7a77c596803b65d8cc9`  
		Last Modified: Tue, 10 Dec 2024 02:00:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-alpine3.21` - unknown; unknown

```console
$ docker pull postgres@sha256:b071765c577efbe5d368b4ffefa1dc436a38385994c14158bada20695b2d2af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.4 KB (638387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7ea1c68401c74732ff3fd85414fb811bf2d6a4dbfbd797d1d482746bf0ef26`

```dockerfile
```

-	Layers:
	-	`sha256:3eb59620059f79a477e96a49446e2382c254715bf9f91cf8cacab52450ce9bbb`  
		Size: 594.6 KB (594572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74af37f3030957df7d0a0b73755087189cf6d331f12a4e733eb86ccb794bf1af`  
		Size: 43.8 KB (43815 bytes)  
		MIME: application/vnd.in-toto+json
