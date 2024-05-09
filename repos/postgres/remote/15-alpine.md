## `postgres:15-alpine`

```console
$ docker pull postgres@sha256:b1d85c5f0ef492daec67dcd5488791f6ef2a5ed7618b8a7034d176d517c6ce99
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

### `postgres:15-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:5e47640465cdd6c5745c7a4a4a5e8742ac22f747167383fb6929ea305474ad30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96898844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bfe92fd0d3449218173fecb1def9edb8720b5d7bd6f13c756a174c7de5269b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7db17837dac1724966d3f8d07d11b722b9f969cb0add214e46d6e8b584b7caa`  
		Last Modified: Thu, 09 May 2024 21:56:47 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e397c214555b068a47e16caf6c89a980cd3dd4d7a7882c2362c8147b1e3e3a4`  
		Last Modified: Thu, 09 May 2024 21:56:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0993af0bf89a2857170249e1be7f4e25c8dd0819f9a151ff86d40381bdf825`  
		Last Modified: Thu, 09 May 2024 21:56:49 GMT  
		Size: 93.5 MB (93473380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19fe534f07fcbd52194a1800850ecf847146560496f4f394d053d547f106bc9`  
		Last Modified: Thu, 09 May 2024 21:56:47 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a866bde633ed4842475adadc6bbdc2c5661d65f2064d26ecbf5a750afe7384`  
		Last Modified: Thu, 09 May 2024 21:56:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6295d16daa4afbf741bbbb6b044ba2965d9225736d0c566b2c19cd82695173`  
		Last Modified: Thu, 09 May 2024 21:56:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153bf4c34e0d5860df0f117b508cdeee3beee18a3ec5bb51001b7365aae315a4`  
		Last Modified: Thu, 09 May 2024 21:56:48 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38be918f18327a3ec6103cb0a3927664b02881fef3640193d482c85f63957843`  
		Last Modified: Thu, 09 May 2024 21:56:49 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:35d9b3fb5e3da32278211c18acbe163b4259f72295314fc33fb6e17cb4d49eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **995.2 KB (995160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8901ba8b6aa881a40f108112896f5f147877ccb0ba2f62a1e014306421811661`

```dockerfile
```

-	Layers:
	-	`sha256:343284b33596594c6c48436ffd327218b67fec2f4f901661a6c0aa931dc96136`  
		Last Modified: Thu, 09 May 2024 21:56:47 GMT  
		Size: 957.3 KB (957311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b91a144464521ced7f4dd70436f8e7919257e49e33e36974eeb770db0f9a44e5`  
		Last Modified: Thu, 09 May 2024 21:56:47 GMT  
		Size: 37.8 KB (37849 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:e775db07b08bb13a6ac2dd006356eba8a21a1120a1eb44b3d553bca2b52a1b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95365522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760632ed11f4a185e4796ce27774f1361b3df1cf77b7304257ab3a20cc91f966`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
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
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b675d45afe983b29c7135f33138e534ba9aca9ca6d05d28e546e09d1e6bba8`  
		Last Modified: Thu, 09 May 2024 21:59:43 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4f6c09ac2d383e82b8fba12dd71c915fd20ddea25bd838ee27c29df1a0982d`  
		Last Modified: Thu, 09 May 2024 21:59:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad25f991ee2d28bb92b186403761c98c448815ba0956905668e4407a5efa49d`  
		Last Modified: Thu, 09 May 2024 22:06:26 GMT  
		Size: 92.2 MB (92183397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989c75b3395fb3f0d23fa0d38f9d597fe2bd81c26509972ea37c47e7c87c9f83`  
		Last Modified: Thu, 09 May 2024 22:06:23 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84c17a6f3f7670e38746486d76984e21149f4413d3d9c43e693fe56b7083df3`  
		Last Modified: Thu, 09 May 2024 22:06:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa056f46d026adab2cd0df0e857062f25594159503b951bcfa50875dee2f0e1`  
		Last Modified: Thu, 09 May 2024 22:06:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc145f6de726afdb800cc0bddb7293de59f50b673e0e8026da64aeb057b64c27`  
		Last Modified: Thu, 09 May 2024 22:06:24 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc63cbd879f2db0be76af8c6a026e7c3b3f357bf140fa597b28549dde2a2fb1e`  
		Last Modified: Thu, 09 May 2024 22:06:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:1ce9fcfa75fc48632a58278ab0b3d158460811f5211d8476936841e13b1b5c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd4f32771c1c40011fb91dbd01268b301fec48a7fdc6d4b1b9398a0b0eff926`

```dockerfile
```

-	Layers:
	-	`sha256:9660bcb77780e333a94ee207382332fb6b142ce3c6e115a18f57d5b550576d41`  
		Last Modified: Thu, 09 May 2024 22:06:23 GMT  
		Size: 37.6 KB (37612 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:6149bb3f785a6b8eedd0ce028f574e6175be6d454859bea693c4b4bc809200e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88056529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b78dc6a080a1886fb5d6f0b4fbe42e6d6cf5d9f053d75770153f9253033c84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_MAJOR=15
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_VERSION=15.6
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_SHA256=8455146ed9c69c93a57de954aead0302cafad035c2b242175d6aa1e17ebcb2fb
# Thu, 08 Feb 2024 19:40:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:40:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:40:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:40:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34183be10276d5bf28456f8dfa0b74b7d3728c5cf15e6e32a1203d02c80f06ed`  
		Last Modified: Sat, 16 Mar 2024 16:21:42 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bfc51b527ab2c0a5829fb7c7ccd2555218ae3b9c54fce2f19c92a88f06ebe1`  
		Last Modified: Sat, 16 Mar 2024 16:21:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a9475030b738adb9ddb518700564d3286e389189e5788bb2495e1a8f16d4ea`  
		Last Modified: Sat, 16 Mar 2024 16:32:27 GMT  
		Size: 85.1 MB (85120900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80b10cddefa468c3e74ce3948cf401aafc01278041da8e48eac8b9499da44d5`  
		Last Modified: Sat, 16 Mar 2024 16:32:25 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41d6b1e2b24101616cf50c591988b7f9a7730ad56d9ebcbe6b971c6b1c31f7c`  
		Last Modified: Sat, 16 Mar 2024 16:32:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461b5646b1ccb4bee277075a5a1090ad7a70d8f19af1359d8709999d53cbe8e4`  
		Last Modified: Sat, 16 Mar 2024 16:32:25 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af166ae1257311dba74496546c778c5b119181000d651aabedfecc0709cdf785`  
		Last Modified: Sat, 16 Mar 2024 16:32:26 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be321018592f90111b74e22c12b32bacf201c00125f08ed4188be4e69a7ee93`  
		Last Modified: Sat, 16 Mar 2024 16:32:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:5dff2f03ff1a9df8996b1737033deee602a4dec4f355fabcfd9434902e888a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **995.2 KB (995170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad6ed0c49b1204de85f5f89a279775324b8503856a8c8e96b7a5468ef3b53fb`

```dockerfile
```

-	Layers:
	-	`sha256:ee07c5621522e4bf8e06a56e91134cda84e363991206d0a6d12075d522277ec1`  
		Last Modified: Sat, 16 Mar 2024 16:32:25 GMT  
		Size: 957.3 KB (957343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60f854ae32d369c931fde42a99e7612ab21ead2eb01c9928e627cfd8376482e8`  
		Last Modified: Sat, 16 Mar 2024 16:32:25 GMT  
		Size: 37.8 KB (37827 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; arm64 variant v8

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

### `postgres:15-alpine` - unknown; unknown

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

### `postgres:15-alpine` - linux; 386

```console
$ docker pull postgres@sha256:219a7ba137b9dd63fee42acb58d2136573fa439f41af3bd68498e124c505849e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102042308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee6e1c0ec11044992253d31d5c1bc645d5e51d810dee49e2976f8c74d0c46d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
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
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3ef5f68db12421d78821e3ed4227954ca8141736648051f8d74d908a8fb4f9`  
		Last Modified: Thu, 09 May 2024 21:57:08 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e397c214555b068a47e16caf6c89a980cd3dd4d7a7882c2362c8147b1e3e3a4`  
		Last Modified: Thu, 09 May 2024 21:56:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2948bdbe9de410b03e75703f9162da117ca7a5c238e25ee8084bcdf62161035`  
		Last Modified: Thu, 09 May 2024 21:57:11 GMT  
		Size: 98.8 MB (98781490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6337f60f035a8c3b5e372c116fedf8b9aa149e29baa4675e133139be3fbfad90`  
		Last Modified: Thu, 09 May 2024 21:57:08 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25215a3b18b6d71e607d1a39a2b62ff23b504eb33b119fa975d5dce8aebaadcf`  
		Last Modified: Thu, 09 May 2024 21:57:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049a7bff6f1b6d6ba403a6a0c7b1b0dad836d8caf2f208eb5431f29a3853c4d7`  
		Last Modified: Thu, 09 May 2024 21:57:09 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b26c3c95680b1e59ee12feff1041c6cd91563eaabfee4dc7d291de9d17d701`  
		Last Modified: Thu, 09 May 2024 21:57:10 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac5de88293494faf155d8171b31ae0387bf6b6f2dbb294048ab29192654c57`  
		Last Modified: Thu, 09 May 2024 21:57:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:d476fb6a66f13ae65902e593a2deed965873311f92379e495e0bf44eacdee4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **995.1 KB (995093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15472bea5ccf0e07f1309bdaed65164d6a03e5964789f0c354421a7f3bb1802`

```dockerfile
```

-	Layers:
	-	`sha256:8766f1660eff3804277a0f10a33efefea8d3d0109bac8b6d57fc390f76b7ef14`  
		Last Modified: Thu, 09 May 2024 21:57:08 GMT  
		Size: 957.3 KB (957286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7168edb5235094be9b7104506f2c82c114d6fcb8f072820579b369d36a0bab4`  
		Last Modified: Thu, 09 May 2024 21:57:08 GMT  
		Size: 37.8 KB (37807 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:72c012e32a9261809e0ba4d9656193505c9599ae2a085b80684309fa20bfbf97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99445810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2255f9a7c32505993a0b2a090f6b75255b97cb2f87cc82bd0ee0b3888a48661b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_MAJOR=15
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_VERSION=15.6
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_SHA256=8455146ed9c69c93a57de954aead0302cafad035c2b242175d6aa1e17ebcb2fb
# Thu, 08 Feb 2024 19:40:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:40:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:40:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:40:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79df8127be221428a326f357e04f1c6c7907b2ac1145408ba7f22a36fe89ce2`  
		Last Modified: Sat, 16 Mar 2024 10:37:24 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e0b43ea44af8adfb383299b0e1e2f4fdbb58b567f44792024513de6b0a73dd`  
		Last Modified: Sat, 16 Mar 2024 10:37:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627dbea9a2de11c18b8cf0f7b58867d2883ee27c59b750c0b0cd2aa137f285e6`  
		Last Modified: Sat, 16 Mar 2024 10:43:38 GMT  
		Size: 96.1 MB (96070721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a94424ecd9b4e7ddb9bd5c61daa8ac4fb7d4acccdc701198964237c5baf8f25`  
		Last Modified: Sat, 16 Mar 2024 10:43:36 GMT  
		Size: 9.5 KB (9456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070fcd38cb8397a08a39646e63df29dd249caac6f0bbb2ae061cb835e4d119ed`  
		Last Modified: Sat, 16 Mar 2024 10:43:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e80bbc6d5e65cd7b5836606d8ad9b1257496a80a3a51b79978244a8efac681`  
		Last Modified: Sat, 16 Mar 2024 10:43:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f945e3da78b5a8a224581b510c2c7c7bd6fe7caebc9fbe3ebeb8ad1e00c4f66`  
		Last Modified: Sat, 16 Mar 2024 10:43:37 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1427f053ddd23e89181d89a2c1a473eabd8e3aabee2a15305e592656855727`  
		Last Modified: Sat, 16 Mar 2024 10:43:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:b1d2419d641c2e9bd789b70ad3be471abf44be6b86d503d971685fd0ed6a6400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.6 KB (991595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2000bf770112aa44381174790e33f269da2470ad0f389da45b6e4cae448244ae`

```dockerfile
```

-	Layers:
	-	`sha256:235e4795bda1df83644fa0ba7a70a229080b59b2e6fbf23f712459475c4ae11c`  
		Last Modified: Sat, 16 Mar 2024 10:43:36 GMT  
		Size: 953.9 KB (953866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5bfa8afebf567c4cd102257e05981845b13806e631d389abc001023a3effc1c`  
		Last Modified: Sat, 16 Mar 2024 10:43:35 GMT  
		Size: 37.7 KB (37729 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:0224c7b555c2892092bde30da940281d615e108bab44c458ddfa4bca2909814d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105579254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e920b71fee4af95a2ce7d8eda0fc00dcb335c0807ab698bec0d2da3150c79a21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
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
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5640c2be82ac04ba5ddac695379fa624aa02fd3579b534fff1c3dd4eba189313`  
		Last Modified: Thu, 09 May 2024 22:13:40 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85541a3a0f2695e7b89ffb03367e1f86a74f6ff41d24e68ce35f629a057ca65a`  
		Last Modified: Thu, 09 May 2024 22:13:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbae3c6fe6066779cafe442745aaf1e96d0ac7ffa2a70cc44254a294bd0bfd3d`  
		Last Modified: Thu, 09 May 2024 22:24:19 GMT  
		Size: 102.3 MB (102319884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21464b78af0545350916a4e1d70d2def2bd164972b81552e9fa34ab4d269516b`  
		Last Modified: Thu, 09 May 2024 22:24:17 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c840ad50d3c73bd851c580b280627a69a614e09a26c6ca973c0714e3e509d39a`  
		Last Modified: Thu, 09 May 2024 22:24:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b91f0ea0be8adcfac995e823852346a7df78c691db063a47d5a149d76784e3`  
		Last Modified: Thu, 09 May 2024 22:24:17 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ead1ef72c5712a625ffb714a36b1822f5a195b5c137e7f3fd7d2314d6a8aef5`  
		Last Modified: Thu, 09 May 2024 22:24:18 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef2455baffe5d32cae29b532437a8410ffb24552fb73fa969ac4545ff839d0d`  
		Last Modified: Thu, 09 May 2024 22:24:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:cd5216df38d38f26e8d5bedd2bfdddafae02c6364857606b0bed768376df7af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.0 KB (993046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1940f32248d7d0ea89c4e87505d53ccb1c875573e79dd73499669e67b355457`

```dockerfile
```

-	Layers:
	-	`sha256:26cf65242d161af15bd59762f4bde9707c3b6e5829e47b3ce76018256f10f593`  
		Last Modified: Thu, 09 May 2024 22:24:16 GMT  
		Size: 955.4 KB (955357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3fc34908aaa68b9f5ccd1d461e87c11882fd8a19a32d5e514688bee6b29e48`  
		Last Modified: Thu, 09 May 2024 22:24:16 GMT  
		Size: 37.7 KB (37689 bytes)  
		MIME: application/vnd.in-toto+json
