## `postgres:15-alpine3.19`

```console
$ docker pull postgres@sha256:8df6d642013b02bcf8ad04dd8c98d2597c56375c7566fcca370f9b35cd61a159
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

### `postgres:15-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:d2d35a5e0a38d4d0bf565e7552499e1de3e590fcf22b1410b002a26d297acce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96887878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9655dd4ce3e3f59ab3e22b5ffcf4332d1bb28d95646e903d4b88c9713243669`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=15
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=15.7
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8defc9dd8ba7c5b8814e50b14b8b461bdfe3edb1628b7ce954455e519d3fb5a0`  
		Last Modified: Mon, 03 Jun 2024 19:06:19 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c78bc305665efce90487e754c6ca66d26a6d771f91d41d3e72ca071d4c31ced`  
		Last Modified: Mon, 03 Jun 2024 19:05:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7854e350acde5439d01fdffba4497047ad04ca577c13d2a0e5195db9797965ad`  
		Last Modified: Mon, 03 Jun 2024 19:06:22 GMT  
		Size: 93.5 MB (93462413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee67894f16d9faf7e7ee211e0d98dbad613ef55042910277fcc1ec8422b1f602`  
		Last Modified: Mon, 03 Jun 2024 19:06:19 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026d7eb5eff8c354f1148fdae6a0bbbf20423e7de0da85da88a8dc069a3d6489`  
		Last Modified: Mon, 03 Jun 2024 19:06:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968a3e816ae1814dfaf84fcc9e33311dc0283e5f0e30c26a7a679957f1cc980b`  
		Last Modified: Mon, 03 Jun 2024 19:06:20 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b135e54cb3a0ebc78dfec61abddb4ea7b1eb241721e928f5c7e735a0c6e3d581`  
		Last Modified: Mon, 03 Jun 2024 19:06:20 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71671c2dc720c719cc6fdb0ba2e63ee783d901a33a1b2b6776b1fdf355068673`  
		Last Modified: Mon, 03 Jun 2024 19:06:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:ad23608a860a044f7ebd43cfb38d2e4cd061321c7ff14b90f158e5f4ff737951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.8 KB (993773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24d918ddfbb814be00455acacbea8720a53fa8aa1fe067aef63eeb1da260e5b`

```dockerfile
```

-	Layers:
	-	`sha256:74dab1e7650575ef9c499a8c9f31733513b4654003354295e672ab35497b74e8`  
		Last Modified: Mon, 03 Jun 2024 19:06:19 GMT  
		Size: 956.7 KB (956690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fc7b8d503ed6a3a48ac8f04c1fa2d177c691e637c11b17f34b6dc20095ada71`  
		Last Modified: Mon, 03 Jun 2024 19:06:19 GMT  
		Size: 37.1 KB (37083 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:8b4b42cc038c6bbe97d9d83bc709a394c7454e75253dd7cef02bf01752df6b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95356660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2854d3b9cb54f938cff761675bba38fbf6f9a5def618a9a311b6e531f8414f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=15
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=15.7
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860e35ae27435bcb376652f33da561573efc82cb903cc30ce3684aff0ca6d38b`  
		Last Modified: Mon, 03 Jun 2024 19:26:27 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a305f8be1993a674347a47e4e4da6dc04c8b7969a73d6830b0cfe4e8de939888`  
		Last Modified: Mon, 03 Jun 2024 19:26:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8c53d1fa71f231da2a2376c565ebceab1b5df6098636cf28c8a80dc7b8a568`  
		Last Modified: Mon, 03 Jun 2024 19:43:05 GMT  
		Size: 92.2 MB (92174527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f587632e1348e4db8b49f22daffc0c9ad8f94479fd5260914b847c69706ffca2`  
		Last Modified: Mon, 03 Jun 2024 19:43:02 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3ea5d48c7a3dd1f3c6285d6599f5feb965e6110670899059edd634ac812f5b`  
		Last Modified: Mon, 03 Jun 2024 19:43:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8b91b534053d6f162308aeb7270d6e19f4fd10e81855c8f35a5cf3a4120dfd`  
		Last Modified: Mon, 03 Jun 2024 19:43:02 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad03d9098a8653b9553adf9bb5a06e6b0f3c03960018058eef44eb20baabd32`  
		Last Modified: Mon, 03 Jun 2024 19:43:04 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd393440dbbd1349c242d8d39c7b55aec64a199972ad492d98de4561f06e46fe`  
		Last Modified: Mon, 03 Jun 2024 19:43:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:d2cfc13702876a0941b3349f1bf35a63e024a9a38eb0d6b5e078b7e0e948b267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 KB (36996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6193eddfde298d19b1a1f3d06a74997dbdca6c5d90a696f2c30be0aadb5b6b62`

```dockerfile
```

-	Layers:
	-	`sha256:4012b838841b39226cfe25d6a4b476f2b5715ad3651d4d38f8d10d01bb3c9bf3`  
		Last Modified: Mon, 03 Jun 2024 19:43:02 GMT  
		Size: 37.0 KB (36996 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:dfccfbaa658f62b03de0cc9c26dcad604505d1d5dc1980f9749758ad301c4216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89692803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5efee7429abf349d5a100a027e35c165abadbc132fa2eabca25024ad259a685`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=15
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=15.7
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e4bfd7c0deff5a703442b05eea3fc3238bd197ba703ae949a0a735a738790f`  
		Last Modified: Mon, 03 Jun 2024 20:42:33 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6f980339956e09a15f739f93841e0d33b8e50c83f4e1c2c83dd4ead7ef7a6`  
		Last Modified: Mon, 03 Jun 2024 20:42:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c46e81901ca4d8cf82948f7af721d76af6ecf72f9ee1cf762f6dab9c9160504`  
		Last Modified: Mon, 03 Jun 2024 20:56:13 GMT  
		Size: 86.8 MB (86757169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6459ce3ae4545da237bb6d5d765f7b36d9ae62f7813d56e4d3ccca9b8fb96a7`  
		Last Modified: Mon, 03 Jun 2024 20:56:11 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09f6d65e9aa425fe7b45f32f035e1196174421c3df0d4471bcdb3984012b693`  
		Last Modified: Mon, 03 Jun 2024 20:56:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002be3e77729595f4c2d9a477326793f11ea19be6524dd94c764b94ee2286c54`  
		Last Modified: Mon, 03 Jun 2024 20:56:11 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5079a54dc55f118a81a6c479722ded03ca12906a30a8938e946b3f1f0411ea65`  
		Last Modified: Mon, 03 Jun 2024 20:56:12 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61093b5c459a1806702b180450210acd6ba4987ef0343e75b9981d9c49ee849`  
		Last Modified: Mon, 03 Jun 2024 20:56:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:ffae25016bd71044d2305f17ae68df7dfa060ab3e59618302df3d88d3f9f771b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.9 KB (993925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bafdf7dbd9fd577c1c35edb91d2bc4dc1dee90f6efa55247b28f28ae6077be83`

```dockerfile
```

-	Layers:
	-	`sha256:b2932c6428d32c298e206f4edee5b36a6d978f1979cfd8d0f67757def834398b`  
		Last Modified: Mon, 03 Jun 2024 20:56:11 GMT  
		Size: 956.7 KB (956710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d0fe5aa73e55a2c98d063a7216b5388b138ceb06a7f9072cec87b1198451b6`  
		Last Modified: Mon, 03 Jun 2024 20:56:11 GMT  
		Size: 37.2 KB (37215 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:e9b041e6c84c42ddb30f8bcfe050cac1a3f1dd1079db9d3ffbff3fb0e573696a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95547875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43577b2f2c6dc39f4dc9b923f8610fbc9465ae61ac3e5846f6a10c0a3ad3ea0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_MAJOR=15
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_VERSION=15.7
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Thu, 09 May 2024 18:44:17 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:44:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:44:17 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:44:17 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:44:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6426790b86128c81359671377728ac209ddd73d25d62a98505f61e0f34e541c2`  
		Last Modified: Thu, 09 May 2024 22:23:47 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2765e6e641bc36e3e37080f48cbbeb6eb6beb085e0a5cc4d749578ec2b27d79`  
		Last Modified: Thu, 09 May 2024 22:23:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc68123572610ba14f7cadc0e910e578520354589d27235767c358946b0d6e2`  
		Last Modified: Thu, 09 May 2024 22:31:50 GMT  
		Size: 92.2 MB (92183426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c9317f684340ebfabb943a4233becd1aa1bd401afa1b5c64b73e3fab3810c8`  
		Last Modified: Thu, 09 May 2024 22:31:48 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad68caa58ca3b786b6450370941739c61e5a4b10dc4f90b780de2ac635e8ed8`  
		Last Modified: Thu, 09 May 2024 22:31:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167d5bbfa5809043eb2f0f7528253558f3d2ed1257c21bb8746a4c06209c9a06`  
		Last Modified: Thu, 09 May 2024 22:31:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f266fcd3a4f2af95c9a6e85dfdcd764dab813b6d1fd62c92a41642b41431ed5f`  
		Last Modified: Thu, 09 May 2024 22:31:49 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed5f49315bfd1e3be0d76dc664069126c8ad57bbe176497f713a91faf7e17d4`  
		Last Modified: Thu, 09 May 2024 22:31:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:4381f15c03c4703134a83e1ed33c8152d3814c081e5f1c89bc8f430953f8705e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **995.0 KB (995015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c807bfade6eb70f37e8cb58c4b0e54fa6a33ee8c367a954ac7cc62f272ac081`

```dockerfile
```

-	Layers:
	-	`sha256:3b84670690a1a8f98013478c67f08f570b836a9fa38eb230b5b0a2c42a6dbccd`  
		Last Modified: Thu, 09 May 2024 22:31:48 GMT  
		Size: 957.3 KB (957322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:709740d1ee6d9e2f72705f4791ccd3fbf2e13229f30113b41432f4552137cd4b`  
		Last Modified: Thu, 09 May 2024 22:31:47 GMT  
		Size: 37.7 KB (37693 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:108bb78193d0c7054e3ebf076178b3360e807b0080cd75dad40596d17140839c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102046254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7307285c08c33e415f224113777560e35f73cd6cf90fa44c330f4274e29ea55f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=15
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=15.7
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9807f98f2129694d80884ec8caa1b87943e741157a445a049dfb9cee5b74bae4`  
		Last Modified: Mon, 03 Jun 2024 19:06:25 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d43d347f790fc6ee6f696cda958ee4f37470aa355e7b9513bf545699486565c`  
		Last Modified: Mon, 03 Jun 2024 19:05:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0079143d30bd9b0d8248a9bcfaa5c4c864af5a47fbafd5f67068175a37cb86`  
		Last Modified: Mon, 03 Jun 2024 19:06:27 GMT  
		Size: 98.8 MB (98785432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b41b12990f60fde4017ce86af405c4af4da7b746c6ee66699fcd293ef6107c2`  
		Last Modified: Mon, 03 Jun 2024 19:06:25 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393de5dda1d0b9f40e418ff6b68036792b21ef838f37daeaa60140f99509f747`  
		Last Modified: Mon, 03 Jun 2024 19:06:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889a8f096276316b953b6bcd246e1a3b92da966e1b525f60a708a3d103e06cd8`  
		Last Modified: Mon, 03 Jun 2024 19:06:25 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2c225d1573c34d3915fe462a506b411bb8126d2bcf73427bf6eaf7372ae4af`  
		Last Modified: Mon, 03 Jun 2024 19:06:26 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af11c1c381f84c3505d81a16cd3ec4a645af171058d8fa8270b1a484146dd9ab`  
		Last Modified: Mon, 03 Jun 2024 19:06:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:8504b63033dd019c8b1834bbd80826840f3ffab7e6ee7528db5e81f1008c6527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.7 KB (993727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54022cb77bdad6a33ce2a7ae295e49d01b549dadb90783d70cc1761eccf2a21`

```dockerfile
```

-	Layers:
	-	`sha256:04a5c2d5366adb9d84a53e74ec4f2ef46af4e3dd0dcaf883be532f18c88cc65d`  
		Last Modified: Mon, 03 Jun 2024 19:06:25 GMT  
		Size: 956.7 KB (956675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d3aacba5d58a56a18f03d08eb35f322542aa35231b0b553a6034538f1e21e70`  
		Last Modified: Mon, 03 Jun 2024 19:06:25 GMT  
		Size: 37.1 KB (37052 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:960ca1533df0cbc0ef638d8f9f75ec9b6929767a39754ca00726c545e8a898bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101400284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7147f7cf5ca73d13ec9e9df95dcb2abc0a3054ab4cdb4e4c2a6af108d1a7ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=15
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=15.7
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc0a98c9d584f2a67805c2d06416946139d1fc100fbde03f3fb69498d4adc87`  
		Last Modified: Tue, 04 Jun 2024 00:41:59 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46b4079b8ab65d67e0592c39b5171188bfa6367e02f4dd92f69cdf45d9ce755`  
		Last Modified: Tue, 04 Jun 2024 00:41:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f665fdacea99468f831ff6a01698695552ee170c3748fa1704ec478e8a07cd6`  
		Last Modified: Tue, 04 Jun 2024 01:14:59 GMT  
		Size: 98.0 MB (98025192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa42cc623ca32755326604199ca92f4c3c637c53a6fae5e3dcd19eaf23eb95a`  
		Last Modified: Tue, 04 Jun 2024 01:14:54 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15eba9217c21d3fd85e09fb378e00b2f736e0c25f3c0b661acf51fa494c463e8`  
		Last Modified: Tue, 04 Jun 2024 01:14:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ecd78440ce5812a304a08bd58e1c76e5e37e23ba1a3dc829df5bde00cfb7f0`  
		Last Modified: Tue, 04 Jun 2024 01:14:54 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e07750a496aaf4788ca0a073518dac9eaec80600893bd3d2ae62079d00befeb`  
		Last Modified: Tue, 04 Jun 2024 01:14:55 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b000b3588bb2af4fdba82fb07e70179de8357b95f6e3aaa733ebd637b93e81`  
		Last Modified: Tue, 04 Jun 2024 01:14:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:6995e317bf43fc0aff54c056635da9e7924f57f64c1332468be585f666906e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.4 KB (990358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775caffda5062aa7204f2ab93f7ad6dc99e012574afc1f0e24ca70045c87fc75`

```dockerfile
```

-	Layers:
	-	`sha256:0cc66199a07845b2f927a7268154e111a5954d16077ebf48bba020e878ae6205`  
		Last Modified: Tue, 04 Jun 2024 01:14:54 GMT  
		Size: 953.2 KB (953237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c11ff44c111c895ea6b5a4dea92885eed8fe0080bba3ad1f082956873b8ec071`  
		Last Modified: Tue, 04 Jun 2024 01:14:54 GMT  
		Size: 37.1 KB (37121 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:5206dfcad9601fbf30f5bd5e88579984c70ad57da56ee968d11753a504ef0d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105578806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ad45e07330e7af749acd7846b99ce12be438b562820496709d55cb00242340`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=15
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=15.7
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddf070e1afb1dfa2858898d44cc73300f9c817c9455e866395af0ebaadac77a`  
		Last Modified: Mon, 03 Jun 2024 19:55:56 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9d3e69e197d6e0a5091fd3be948bac07f0cefefb29f336d0fc54d6ba476000`  
		Last Modified: Mon, 03 Jun 2024 19:55:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa1d26e3af8b7cf06d68944f51b8b99d16a8b1c34c1abaf9a6475f1bd3c0747`  
		Last Modified: Mon, 03 Jun 2024 20:34:56 GMT  
		Size: 102.3 MB (102319430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da0b38d5cd39ba6f3ef97f3cc205137828c35f2fc3968fdda6812b20e87700e`  
		Last Modified: Mon, 03 Jun 2024 20:34:54 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14b5cff72b435ae7defda3991281f1e79217e8ba6c2ccf62f4560d5131fafaf`  
		Last Modified: Mon, 03 Jun 2024 20:34:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dd31dbf91ad01a3544ddae569139fbe5d4b1c7782d7fd289e50fab26092375`  
		Last Modified: Mon, 03 Jun 2024 20:34:54 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d8a78d74befbd244e0f9e7b50177596420bbfb4ef3d9205e679d381b89f4c6`  
		Last Modified: Mon, 03 Jun 2024 20:34:55 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d37aa154778f3f30ba693170ed56027f1721d915f1211ab84d5e80bb44b1cbf`  
		Last Modified: Mon, 03 Jun 2024 20:34:55 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:7a44b87d912787d59ccdd467e5156640b6e60dd9d7a94bf087248f6dc8b465fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.8 KB (991822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cfc64f37676b8ed3da0176cd1c01ee759cb2f5334b6267aa4409c6066ced0e3`

```dockerfile
```

-	Layers:
	-	`sha256:19f043efbcbbe886dc0b31dd29f9200625b20740181f4424893bfb3ca0e28653`  
		Last Modified: Mon, 03 Jun 2024 20:34:54 GMT  
		Size: 954.7 KB (954736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7084c0e71cea307315a0411899e236aad9fee6c722b10f863a0bcf8db739e3be`  
		Last Modified: Mon, 03 Jun 2024 20:34:54 GMT  
		Size: 37.1 KB (37086 bytes)  
		MIME: application/vnd.in-toto+json
